
<ins> 05/11/2018's meeting minutes with DR, YC, EC, JW, BL, OM, DH </ins>

#### Generalities

* Capsul, soma-base and soma-workflow have been added to the Populse GitHub project

  * Quick reminder: soma-base contains some generic tools that are used in Capsul and Brainvisa

* Should we change the name of the several repositories to maintain a certain coherence ?

  * Either rename populse_mia and populse_db to MIA and DB

    * Could be too generic (hard to find the database API by googling only "db")
    * These names already exist on Pypi

  * Or rename Capsul, soma-base and soma-workflow to populse_capsul, populse_base and populse_workflow

    * There could be too many dependencies to change

  * This point will be on the agenda of the next meeting

#### Populse_MIA's deployment

* Bring together MIA's current config with Capsul v3's platform

  * There should be three levels of config

    * system config
    * user config
    * project config

  * The user config could be initialize when the software is launched for the first time

    * The user could set the different default values (e.g. to use SPM, FSL)

  * The project config would inherit the user config and would be specific for each project

    * The project config could specify where are the data, the modules to use etc.

  * The user/project config corresponds to the Platform object developed in Capsul v3

    * We should rapidly agree on the development of this API and its concepts (e.g. what do we need to run SPM)
    * @sapetnioc proposed to create a feature branch on Capsul's GitHub repository with the Platform class

* Populse_MIA's architecture

  * Two choices:

    * 1: keep the same architecture and create a name_of_package.py file in "populse_mia/python/populse_mia" importing all classes in the package

      * e.g. in data_browser.py: "from src.modules.data_browser.count_table import CountTable" etc.
        * So we could write "from populse_mia.data_browser import CountTable"
      * Even if this could avoid to change all the architectures, this could lead to circular imports (not sure)

    * 2: change the architecture to put everything that is under "src/modules" in "populse_mia/python/populse_mia"

  * Option n°2 has been chosen

* How to deploy/install Populse_MIA?

  * This is not a simple question

    * If the Data Viewer uses compiled files, the deployment on Pypi will be problematic
    * This point will be discussed more precisely in a further meeting

* Where should be the main.py file?

  * It could be in the python modules and has to be found by the python path

#### Data Viewer

* Some problems have been encountered by using PyAnatomist on Windows (PyAnatomist being ensured to work on BrainVisa environment)

  * Using a virtual machine could be a solution

    * @sapetnioc proposed to send a "tutorial" about how to set it up


* The specification of the Data Viewer should be added to populse.github.io repository

    * Adding a canvas could be great to start the development of the widget


#### Next meeting

* On Monday 19/11/2018 at 2PM
