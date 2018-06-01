
Modifié le 01/06/2018

Réunion développement 01/06/2018 avec PG et LOB

 * passage en collections(nom collection, clé primaire de la collection), fields, documents(collection, dict de valeurs ou valeur clé primaire) fait
    * comment faire pour intégrer les tags qui sont un héritage de field(nom, type, desc, collection) qui auraient comme champ en plus (origin, unité, visibilité, valeur par défaut),  je pense à rajouté (date création,reputation) pertinent ?
       * après mûre discussion, (faire une collection field, collection tag,  collection de collection, heritage) afin de continuer à séparer le général du spécifique à MIA, mettre sous forme de classe : collections, fields et documents ensuite faire un héritage dont on surchargerait principalement field qui deviendrait un tag = field façon MIA
       * Il faut aussi surcharger la création du schéma pour une base de données non existante, afin d'ajouter les nouvelles colonnes à la table field

Réunion développement 28/05/2018 10h avec PG, DH, LOB, YC, DR

#### Discussion sur populse_db

* Possibilité de créer plusieurs tables pour la même base de données, en créant des "collections"
  * Ceci permettrait d'avoir des colonnes variables (chaque collection aurait ses colonnes)
  * Chaque colonne serait maintenant associée à une collection
  * L'option initial_table pourrait être retirée, et 2 collections seront créées dans MIA (current et initial)

* Renommer l'attribut "column" en "field" car "column" est trop générique

* Retour sur les transactions
  * Elles sont primordiales si jamais le programme plante au milieu d'une exécution (de pipeline notamment)
  * YC propose de s'en occuper après toutes les modifications faites sur l'API
  * database.py sera coupé en 2 classes:
    * database.py: s'occuperait juste de l'engine et de fonctions utilitaires
    * database_session.py: s'occuperait des sessions (toutes les fonctions modifiant la base de données seront migrées dans ce fichier)
    
* Ajout de la fonction "remove_columns" pour enlever plusieurs colonnes en une fois (utile car une table temporaire est créée quand une colonne doit être retirée (SQLite ne gère pas la requête ALTER TABLE DROP COLUMN))

* Ajout de la possibilité de passer un dictionnaire de valeurs à la fonction "add_document" (gain en temps d'exécution)
  * Préparer les bons noms de colonnes au valeurs (hashage) au début de la fonction
  * Passer **dict à la création de l'objet document, au lieu de "name=document"

* Possibilité de choisir la/les clé(s) primaire(s) de chaque collection
  * Choix clé primaire à la création de la collection
  * Afin de pouvoir identifier les documents, il est nécessaire de générer un id unique au moment de l'ajout de ceux-ci (grâce au module uuid, et notamment à la fonction uuid.uuid4() qui génère un id unique)
  * Gestion de multiples clés primaires pas la priorité pour l'instant
  * La méthode "add_document" doit retourner l'id généré du document, afin que MIA puisse identifier les documents par la suite (un dictionnaire scan -> id sera surement ajouté au fichier de propriétés du projet)
  
* Ajout de la fonction "update_document", qui prendra en paramètre un dictionnaire de valeurs, et les changera toutes en même temps dans la base de données

* La méthode "get_documents" pourrait renvoyer un itérateur au lieu d'une liste

* Filtres:
  * BETWEEN dans MIA: Ecriture de 2 conditions réalisées avec les opérateurs de comparaison
  * Equivalent LIKE/ILIKE à faire
  * HAS (NO) VALUE dans MIA: ==/!= NULL
  * Ecriture des filtres pour toutes les recherches dans MIA
  
* Table contenant les "fields" pourrait être une collection
  * Créé par défaut à la création de la base de données
  * Offrir la possibilité d'ajouter des colonnes (attributs) aux "fields" (Serait utile dans MIA pour ajouter la valeur par défaut, l'unité, l'origine, et la visibilité)
  * Collection à gérer de manière différente car elle n'est que partiellement modifiable
  
#### Discussion rapide autour des pipelines

  * Besoin de sauvegarder les paramètres par défaut des briques : réunion à organiser pour en parler
  * Problème de config avec SPM Standalone : besoin de remplir simplement l'emplacement de SPM12 Standalone dans StudyConfig
