# POPULSE: Pipeline Organizer, Project Unifier, Linking Software for Everyone
## populse_mia: 
## populse_db: 
## capsul: 
## mia_processes: 
## soma:
## mriconv:
MRI File Manager allows the reading of some raw and processed data files from MRI Spectrometers : 
- Bruker Paravision PV5 & PV6 (raw data of magnitude type).
- Dicom from Bruker, Philips, Siemens.
- Philips Achieva (Par/Rec & Xml/Rec v4.2).
- Nifti-1 (with or without Json).
- Bids - Brain Imaging Data Structure.

It also allows for converting MRI images to Nifti-1:Export MRI data in Nifti-1 format until 5 dimensions of the image (x, y, slice, frame, temporal).</li>
- Json files are created and associated with Nifti files in order to contain MRI parameters (see 'Irmage Json' page).
- an option of anonymization allows to hide sensitive informations about the patient (name, age, sex, weight).
- adaptation of orientation information in Nifti headers (tested on SPM, FSL).
- option of customizing the Nifti file names.
- possibility to create text files containing bvecs & bvals for MRtrix and FSL (Bruker and Philips)
