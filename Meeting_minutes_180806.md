Reunion Populse 06.08.2018 10:00 OM, EC, DH, LOB, YC, DR
============

-1 Deploiement populse_db
============

- Actuellement il y a quelques problèmes de compatibilité avec python 2.7.
On regarde rapidement pour rendre compatible populse_db autant avec python 2.7
qu'avec python >= 3.3. Puis on voit pour le deploiement avec pip. A l’issue,
 on fait un petit document a partager sur la doc de populse (par exemple), 
 permettant de faire ulterieurement un nouveau deploiement avec pip sans nouvel
 effort de documentation !!
 
 Edit: Populse_db est maintenant compatible avec python 2.7

-2 Sortie de populse_mia du bac a sable :
============

- Faire un pull request dans un nouveau projet populse_mia. On etudie d'abord
en priorite comment fermer les briques maisons. Voir egalement comment supprimer
de l'historique du projet celles presentes dans le cadre du prototype actuel.

-3 Partie graphique de Capsul:
============

- Olivier regarde les codes de Capsul pour pouvoir integrer ce qu’il a deja developpé
par ailleurs ; Dans un premier temps, en s’appuyant sur les connaissances de David et 
ce qui a deja ete developpé dans populse_mia, une liste des spécifications des futures boites 
pourrait etre determinée. Apres validation par l’ensemble des membres de populse (Yann
et Denis etant les auteurs principaux de Capsul, ils auront le dernier mot ;-), 
les modifications pourraient etre realisées dans les scripts de Capsul (a priori le plus
important serait capsul/qt_gui/widgets/pipeline_developper_view.py) en interagissant finement entre nous.

-4 Anatomist / définition des besoins pour le dataViewer de populse
============
- Denis fait une petite demo d'Anatomist :
    - Anatomist est un logiciel de visualisation dédié a la neuro-imagerie.
    - Ecrit en C++ / Qt avec binding en python
    - Site http://brainvisa.info/web/index.html
        - voir Anatomist: "Data visualization and library of high-level neuroimaging graphical components"
        et la doc disponible (user et developer).
    - Globalement la fenêtre principale d'Anatomist est divisée en deux sous-fenêtres : 
        - une fenetre « Objects » et une fenêtre « Windows ».
        - Un objet est en general une image, mais est plutôt à voir comme un objet informatique 
        dont un certain mode de visualisation sera assuré par une fenetre repertorié dans la fenêtre « Windows ».
        - Les fenêtres sont des widgets, ce qui offre la possibilié de les integrer dans un autre objet.
        
- En resumé (peut etre y a t-il des oublis dans cette liste) et de maniere réductrice, Anatomist permet de faire :
    - visualistion de volume
    - visualisation de maillage
    - visualisation de sillon (objet et sous objet)
    - visualisation de fibre
    - visualisation de carte statistique (IRMf)
    - visualistion de supperposition (IRMf sur anat par exemple) (possibilite de faire des overlays meme si les
    2 objets ne sont pas dans le même referentiel)
    - possibilié de créer des nouveaux objets a partir d’existants (fusion)
    - possibilité de dessiner sur les volumes ou les maillages
    - definition de ROI / mask pour les volumes
    - definition de masque surfacique pour les maillages.


- Difficulté d’anatomist : Pas la possibilité de passer par pip car outils en C++
    - En revanche le site web permet un téléchargement facile.
    Il faudra penser a un mode d‘installation facile pour l’utilisateur dans le cadre du projet populse
    (installation unique, plutot qu’un bout par pip puis téléchargement par ailleurs d’une autre partie,
    etc … enfin si possible!)

- A priori pour Amigo, Anatomist a les outils nécessaires pour assurer la succession. Il faudrait que
populse Grenoble recense dans les meilleurs délais les besoins voulus pour le dataViewer afin de valider,
ou pas, Anatomist comme l’API dataViewer de populse. Cela permettra a Olivier de pouvoir commencer a travailler
sur l’intégration de la visualisation dans populse_mia. Si Anatomist est retenu (il faudrait avancer rapidement
du côté de Grenoble sur la définition des besoins) le plus efficace serait de definir un mini prototype de
dataViewer dans populse_mia afin de travailler de concert avec Yann et Denis et petit à petit progresser
dans la connaissance d’Anatomist.

-4 Prevoir une reunion debut septembre.
============
- La date sera définie dès que possible lorsque tout le monde sera rentré de conges.
