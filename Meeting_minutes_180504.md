Reunion POPULSE 10:00 EC, DH, PG, LOB, OM, BL, YC, DR
============

- Compte-rendu :
    - Au sujet des discussions générales
        - Eviter les discussions type "machine à café" et privilégier les discussions sur GitHub pour que tout le monde soit au courant.

    - Discussion sur la sélection des données avant le pipeline
        - Evocation d'un objet DataSelector (qui serait la table du DataBrowser) qu'on obtiendrait grâce à une méthode de l'API populse_db (ex: get_filter_widget)

    - "Tir à blanc"
        - Entente sur le fait de séparer l'"initialisation" et l'exection du pipeline pour gérer la complétion, les formats, les encodages, les paramètres etc.
        - Idée initialement proposée : faire une transaction lors de cette phase pour ensuite commit à chaque fin d'exécution de brique.
        - Cette façon n'est pas forcément optimale car un pipeline peut durer longtemps
        - Idée proposée par YC : tout commit dans la base au moment de l'"initialisation du pipeline". Ajouter également le pipeline (nom de fichier) dans la base de données, avec un ajout de tag "Status" pour connaître l'état de l'exécution.

    - Filtres
        - Un filtre serait une brique, qui prendrait en entrée une base de données (et une liste de scans ?) et un filtrage, et en sortie une liste de scans.
        - Il faudrait donc inclure Capsul dans populse_db et créer un process filter.
        - Comment sauvegarder le pipeline et les filtres ? (problème de droits)

    - Réorganiser le Pipeline Manager
        - Laisser que la possibilité de Save et Load dans le PM (le réappeler Pipeline Design ?)
        - Créer un nouvel onglet Pipeline Processing pour l'exécution (avec les boutons Initialize et Run pipeline)

    - Penser à intégrer MIA2 sur GitHub

    - Limites actuelles de la BDD
        - Renvoyer des erreurs au lieu du code de retour
        - Ecrire un script de test pour trouver les raisons de la non-rapidité de l'exécution globale.
        - Pensez éventuellement à d'autres stratégies (exemple : dupliquer la base avec des lignes de textes etc.)

    - Discussion autour de la licence
        - cf. GitHub pour la discussion
        - Chacun peut écrire quelques lignes sur ce qu'il pense

