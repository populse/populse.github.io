# Pipeline Organizer, Project Unifier, Linking Software for Everyone (POPULSE):
A project aimed to provide pipeline calculation tools to the neuroimaging community.

## [populse_mia](https://github.com/populse/populse_mia):
Multiparametric Image Analysis (populse_mia or MIA) is intended to be a complete image processing environment mainly targeted at the analysis and visualisation of large amounts of MRI data. In this environment, a process pipeline can be easily built by sequentially linking a succession of atomic computation (brick). Pipeline metadata as well as input, output or intermediate data are automatically managed by a database integrated into the environment. MIA is written in Python and is mainly based on populse's API, such as caspul, populse_db or soma_workflow.

## [populse_db](https://github.com/populse/populse_db):

## [capsul](https://github.com/populse/capsul):
Python library to chain algorithms in pipelines
- Encapsulate algorithms in Processes
- Chain Processes within Pipelines
- Execute pipelines in parallel with soma-workflow
- Use a graphical interface to develop Pipelines
- Configure one or more execution contexts
- Embed Pipelines in any Python applications

## [mia_processes](https://github.com/populse/mia_processes):
The official bricks library for populse_mia.

## [soma-base](https://github.com/populse/soma-base):
Miscellaneous libs for the python environment of Populse / BrainVISA

## [soma-workflow](https://github.com/populse/soma-workflow):
A unified and simple interface to parallel computing resource.

Parallel computing resources are now highly available: multiple core machines, clusters or grids. Soma-workflow is a unified and simple interface to parallel computing resources which aims at making easier the use of parallel resources by non expert users and software.

## [mriconv](https://github.com/populse/mri_conv):
MRI File Manager allows the reading of some raw and processed data files from MRI Spectrometers : 
- Bruker Paravision PV5 & PV6 (raw data of magnitude type).
- Dicom from Bruker, Philips, Siemens.
- Philips Achieva (Par/Rec & Xml/Rec v4.2).
- Nifti-1 (with or without Json).
- Bids - Brain Imaging Data Structure.

It also allows for converting MRI images to Nifti-1:
- Export MRI data in Nifti-1 format until 5 dimensions of the image (x, y, slice, frame, temporal).</li>
- Json files are created and associated with Nifti files in order to contain MRI parameters (see 'Irmage Json' page).
- an option of anonymization allows to hide sensitive informations about the patient (name, age, sex, weight).
- adaptation of orientation information in Nifti headers (tested on SPM, FSL).
- option of customizing the Nifti file names.
- possibility to create text files containing bvecs & bvals for MRtrix and FSL (Bruker and Philips)
