Réunion POPULSE 10:00 EC, DH, PG, LOB, OM, YC, DR
============

- Compte-rendu :
    - Logo POPULSE
        - C'est encore un peu prématuré pour prendre une décision. Pour la prochaine fois, chacun peut apporter un ou deux mots clefs que lui évoquent POPULSE et un petit texte de description de POPULSE. Cela nous permettra d'avoir une base pour le futur logo et la description pour la doc.

    - Langage de communication
        - Anglais pour tout ce qui "reste" (commits, issues, etc.).
        - Français pour les discussions de team.
        - On met les compte-rendus de réunion, en français, dans le Wiki de populse.github.io.
        - Dans ce Wiki, séparer les pages "internes" (Local FR) avec le "vrai" Wiki, en anglais.

    - Documentation
        - Dans populse.github.io. Le site web correspondant sera dédié à la promotion/documentation/présentation de POPULSE et de ses modules.

    - Structure des dépôts
        - Avoir, à la racine des dépôts, plusieurs répertoires (/python dans lequel on mettra nos codes (qu'on mettra dans le python path), /bin, /doc, etc.).
        - Les modules doivent fonctionner indépendamment.
        - Ajouter des fichier info.py et setup.py dans chacun des dépôts (pour pouvoir ensuite intégrer à pip).

    - Licences 
        - Choix de CeCILL-B qui est complétement libre mais ne perd pas les auteurs. (Attention au package PyQT)

    - Organisation GitHub
        - Deux groupes :
            - Populse admins : ayant tous les droits.
            - Populse members : peuvent push directement.
        - On garde cette organisation.
        - Concernant les pull requests : on les privilégiera quand l'action sera importante, qu'il y aura une vraie question derrière le nouveau code apporté. Pour les modifications de tous les jours, on push directement.

    - Jekyll
        - On garde ça en tête, pas encore d'idées très précises sur le fonctionnement.

    - Importation de "MIA2" sur le dépôt POPULSE
        - Besoin de réfléchir du côté grenoblois, aussi au niveau du MRI File Manager avec OM.
        - Travail de LOB après populse_db, en plus de l'intégration de la nouvelle API dans MIA2.

    - Travail sur l'outil GUI de CAPSUL
        - Travailler sous forme de pull requests du côté grenoblois.

    - Prochaine réunion le vendredi 04/05/2018 à 10h.
        - Si besoin, LOB et DH peuvent demander des petites réunions d'ici là.
