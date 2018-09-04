Reunion Populse 04.09.2018 13:30 OM, EC, DH, YC, DR, PG, EB, JW, BL
============

-1 Discussion sur l'évolution du PipelineDevelopperView proposée par OM
============

- OK dans l'ensemble

- A changer :
	- Rendre possible de connecter plusieurs sorties sur une même entrée (possible si un switch a été utilisé en amont)

- Voies d'amélioration :
	- Avoir une méthode qui permet de déterminer les problèmes dans le pipeline en direct
	- Utiliser un code couleur sur les liens/plugs s'il y a un quelconque problème
	- Afficher une pop-up en cas de problème
	- Colorier les plugs de la même couleur que les liens, changer leur forme suivant s'ils sont optionnels (carré si oui, triangle sinon)
	- Rendre la couleur orange des pipeline nodes un peu moins vive
	- Changer la couleur d'un process node activé (la rendre plus claire)
	- Lorsqu'un noeud n'est pas activé, utiliser la même couleur que quand il est activé mais plus sombre/grisée
	- Changer l'épaisseur d'un lien suivant son type (image : épais vs. métadonnée : fin)
	- Penser à faire une légende consultable par l'utilisateur
	- Lorsqu'un noeud est cliqué : le mettre lui et ses liens au "premier plan" (griser le reste du pipeline)

- Effectuer une pull requests sur le dépôt GitHub de Capsul

-2 Discussion autour du Data Viewer
============

- Objectif retenu :
	- Faire un premier prototype qui utiliserait la boîte à outils d'Anatomist
	- Réfléchir à l'arrangement du GUI souhaité et à l'interaction avec la base de données
	- Réunion début octobre pour faire le point

- Premières idées sur le Data Viewer :
	- Avoir un browser de la base de données pour drag/drop les data
	- Changer le nom "Image Viewer" dans MIA en "Data Viewer" 
	- Avoir un fonctionnement en fenêtres : chaque fenêtre aurait ses spécificités avec ses propres fichiers, référentiels, type de vues, etc.
	- Avoir une seul barre par fenêtre qui permet de changer des valeurs (contraste, luminosité, opacité, etc.)
		- Chaque image aurait ses propres caractéristiques
	- Faire en sorte de pouvoir détacher les fenêtres (en faire des pop-ups) 
