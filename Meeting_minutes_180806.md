Reunion Populse 06.08.2018 10:00 OM, EC, DH, LOB, YC, DR
============

-1 Deploiement populse_db
============

- Actuellement il y a quelques problemes de compatibilite avec python 2.7.
On regarde rapidement pour rendre compatible populse_db autant avec python 2.7
qu'avec python > 3.2. Puis on voit pour le deploiement avec pip. A l’issue,
 on fait un petit document a partager sur la doc de populse (par exemple), 
 permettant de faire ulterieurement un nouveau deploiement avec pip sans nouvel
 effort de documentation !! 

-2 Sortie de populse_mia du bac a sable :
============

- Faire un pull request dans un nouveau projet populse_mia. On etudie d'abord
en priorite comment fermer les briques maisons. Voir egalement comment supprimer
de l'historique du projet celles presentes dans le cadre du prototype actuel.

-3 Partie graphique de Capsul:
============

- Olivier regarde les codes de Capsul pour pouvoir integrer ce qu’il a deja developpe
par ailleurs ; Dans un premier temps, en s’appuyant sur les connaissances de David et 
ce qui a deja ete developpe dans populse_mia, une liste des specif des futures boites 
pourrait etre determinee. Apres validation par l’ensemble des membres de populse (Yann
et Denis etant les auteurs principaux de Capsul, ils auront le dernier mot ;-), 
les modifications pourraient etre realisees dans les scripts de Capsul (a priori le plus
important serait capsul/qt_gui/widgets/pipeline_developper_view.py) en interagissant finement entre nous.

-4 Anatomist / definition des besoins pour le dataViewer de populse
============
- Denis fait une petite demo de Anatomist :
    - Anatomist est un logiciel de visualisation dedie a la neuro-imagerie.
    - Ecrit en C++ / Qt avec binding en python
    - Site http://brainvisa.info/web/index.html
        - voir Anatomist: "Data visualization and library of high-level neuroimaging graphical components"
        et la doc disponible (user et developer).
    - Globalement la fenetre principale de Anatomist est divisee en deux sous-fenetres : 
        - une fenetre « Objects » et une fenetre « Windows ».
        - Un objet est en general une image, mais est plutot a voir comme un objet informatique 
        dont un certain mode de visualisation sera assure par une fenetre repertorie dans la fenetre « Windows ».
        - Les fenetres sont des widgets, ce qui offre la possibilite de les integrer dans un autre objet.
        
- En resume (peut etre y a t-il des oublis dans cette liste) et de maniere reductrice, Anatomist permet de faire :
    - visualistion de volume
    - visualisation de maillage
    - visualisation de sillon (objet et sous objet)
    - visualisation de fibre
    - visualisation de carte statistique (IRMf)
    - visualistion de supperposition (IRMf sur anat par exemple) (possibilite de faire des overlays meme si les
    2 objets ne sont pas dans le meme referentiel)
    - possibilite de créer des nouveaux objets a partir d’existants (fusion)
    - possibilite de dessiner sur les volumes ou les maillages
    - definition de ROI / mask pour les volumes
    - definition de masque surfacique pour les maillages.


- Difficulte d’anatomist : Pas possible de passer par pip car outils en C++
    - En revanche le site web permet un telechargement facile.
    Il faudra penser a un mode d‘installation facile pour l’utilisateur dans le cadre du projet populse
    (installation unique, plutot qu’un bout par pip puis telechargement par ailleurs d’une autre partie,
    etc … enfin si possible!)

- A priori pour Amigo, Anatomist a les outils necessaires pour assurer la succession. Il faudrait que
populse Grenoble recense dans les meilleurs delais les besoins voulus pour le dataViewer afin de valider,
ou pas, Anatomist comme l’API dataViewer de populse. Cela permettra a Olivier de pouvoir commencer a travailler
sur l’intregation de la visualisation dans populse_mia. Si Anatomist est retenu (il faudrait avancer rapidement
du cotes de Grenoble sur la definition des besoins) le plus efficace serait de definir un mini prototype de
dataViewer dans populse_mia afin de travailler de concert avec Yann et Denis et petit a petit progresser
dans la connaissance d’Anatomist.

-4 Prevoir une reunion debut septembre.
============
- La date sera definie des que possible lorsque tout le monde sera rentre de conges.
