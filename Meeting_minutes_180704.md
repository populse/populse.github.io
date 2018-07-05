Reunion Populse 04.07.2018 9:30 BL, PG, OM, EC, DH, LOB, YC, DR
============

-1 Nom du logiciel actuellement en dev
============

- populse_MIA

-2 Perimetre de populse :
============
- Populse est un projet de developpement communautaire visant a proposer des outils de traitement d’images medicales. A ce jour populse regroupe les API/logiciels suivants :

  - populse_DB => deja disponible sur gitHub
  - populse_CAPSUL 
  - populse_SOMA-WORKFLOW
  - populse_SOMA-BASE
  - populse_MIA => passage de populse_sandbox sur GitHub a populse_MIA des que possible. Enlever toutes les briques developpees en interne dans les plus brefs delais. Ne restera dans la bibliotheque de pipelines populse_MIA que les briques par default de nipype/ Capsul => A ce sujet, voir avec Yann et Denis pourquoi cela ne fonctionne pas par defaut ???
  - populse_MRIconv
  - Un dataviewer, non encore defini (populse_ANATOMIST ? autre(S) ?)

-3 Licence:
============

- Actuellement :

  - populse_CAPSUL => CECILL-B
  - populse_SOMA-WORKFLOW =>  CECILL-B
  - populse_SOMA-BASE  => CECILL-B

- Micro point en attendant mieux sur les licences :

  - CECIL-B: droit francais, la plus libre.
  - CECIL-A: virale
  - GPL: => [Elements releves sur la page wikipedia:](https://en.wikipedia.org/wiki/GNU_General_Public_License)

    "Use of licensed software

    Software under the GPL may be run for all purposes, including commercial purposes and even as a tool for creating proprietary software, for example when using GPL-licensed compilers.[54] Users or companies who distribute GPL-licensed works (e.g. software), may charge a fee for copies or give them free of charge. This distinguishes the GPL from shareware software licenses that allow copying for personal use but prohibit commercial distribution, or proprietary licenses where copying is prohibited by copyright law. The FSF argues that freedom-respecting free software should also not restrict commercial use and distribution (including redistribution):[53]

    In purely private (or internal) use—with no sales and no distribution—the software code may be modified and parts reused without requiring the source code to be released. For sales or distribution, the entire source code need to be made available to end users, including any code changes and additions—in that case, copyleft is applied to ensure that end users retain the freedoms defined above.[55]

    However, software running as an application program under a GPL-licensed operating system such as Linux is not required to be licensed under GPL or to be distributed with source-code availability—the licensing depends only on the used libraries and software components and not on the underlying platform.[56] For example, if a program consists only of own original custom software, or is combined with source code from other software components,[57] then the own custom software components need not be licensed under GPL and need not make their code available; even if the underlying operating system used is licensed under the GPL, applications running on it are not considered derivative works.[56] Only if GPLed parts are used in a program (and the program is distributed), then all other source code of the program needs to be made available under the same license terms. The GNU Lesser General Public license (LGPL) was created to have a weaker copyleft than the GPL, in that it does not require own custom-developed source code (distinct from the LGPLed parts) to be made available under the same license terms."


    => Donc la GPL ne semble pas empecher la collaboration avec quelqu’un qui veut tirer benefice, mais oblige en cas de distribution de retourner a la communaute les codes sources (perso je n’ai pas de probleme avec cela!)

- Ce que nous souhaitons, a defaut d’avoir encore trouve la licence nous convenant exactement : 
  - Completement libre d’utilisation, utilisation gratuite, reprise de tout ou partie du code, droit de modification du code, obligation de citation des auteurs.


- A faire rapidemment :
  - Des que MIA sera sorti de la sandbox pour devenir reellement populse_MIA, le mettre sous licence CECILL (GPL) -> voir pour compatibilite pyside
  - populse_db est deja accessible sur le [GitHub](https://github.com/populse) -> le passer dans les plus brefs delais sous CECILL-B (en attendant la decision finale sur le ou les licences retenues pour le projet populse.

- EC lit la CECILL-B des que possible et fera un rapport egalement des que possible.

-4 Discussion sur GitHub.
============
- On continue la reflexion sur le sujet. Pour l’instant on reste sur GitHub.

-5 Presentation de populse_db
============

- Lucie presente la version actuelle de populse_db

    - Utilisation de cache pour augmenter la rapidite, mais cela revient a ne pas avoir de base de donnees (sauf pour le requettage…) => Possible d’ameliorer sans utiliser de cache ?
    
- [Diaporama de présentation](Populse_db_presentation_04_07_meeting.pdf)

-6 Presentation de la version actuelle de populse_MIA
============

- En vrac, et de maniere non exhaustive, todolist :

  - inclure le filtre d’entree dans la brique
  - gerer l’iteration
  - multi-desktop pour le pipeline manager
  - log (historique, reprise au moment du crash, etc..)
  - sortir les briques developpees en interne de la bibliotheque et pouvoir les ajouter facilement (nous sommes d’accord sur le fait que populse_MIA ne serait qu’un outils et que la veritable valeur ajoiutee sera sur les briques et pipelines. Tout en sinscrivant dans « le libre » pour le projet populse, nous souhaitons nous reserver la possibilite de fermer l’acces a ces briques et pipelines).

-7 Presentation de l’outil developpe par Olivier pour la presentation graphique des pipelines
============
  - 2 points :
    - La partie definition de pipeline est assez redondante avec capsule / MIA
    - L’interface graphique semble plus jolie que celle actuellement de Capsul. 
    - Olivier est d’accord pour s’inverstir sur la partie graphique de Capsul, afin de faire evoluer cette partie. L’idee est plutot de partir de l’existant dans Capsul et de le faire evoluer plutot que de developper a cotes un deuxieme outil de representation des pipelines qui pourrait etre difficile a ensuite integrer dans populse.

-8 Prochaine reunion lundi 06 Aout 2018, 10:00 :
============

  - Partie graphique capsule
  - Anatomist, definition des besoins pour le dataViewer
  - Brainvisa / axone
