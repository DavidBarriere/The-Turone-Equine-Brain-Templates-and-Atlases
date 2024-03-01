# The Turone Equine Brain Templates and Atlases

The current document is a short description of the first version of the Turone Equine Brain Templates and Atlases resources (TEBTA) dedicated to equine brain MRI data analysis. 
For a full description of the resources and the methodologies used to create them please consult the main publication [Valenchon M et al 2024].

The TEBTA resources are a set of standardized MRI and CT compatible templates and atlases meant to support the analysis of multimodal MRI data of the equine brain. 
They were developped as part of the EQUISOBRAIN project, funded by the european HORIZON 2020 Marie Skłodowska-Curie Actions (MSCA) (project number: 101033271, MSCA European Individual Fellowship) awarded to Mathilde Valenchon (host supervisor Matthieu Keller), and by the 'Institut Français du Cheval et de l'Equitation' (IFCE).
TEBTA provide an unified and standardized framework for the analysis of multimodal equine brain imaging data, allowing the reporting of results within a sterotaxic coordinate system.

MRI and CT compatible in-vivo templates have been built from 23 Welsh ponies (12 females and 11 males), 5.7-months old (173 Days +/- 6 days, mean weight 154.25 kg +/- 5.14 kg at the scanning time). Data were acquired by using a 3T scanner (Siemens Verio) onto the PIXANIM imaging plateform (https://eng-pixanim.val-de-loire.hub.inrae.fr/).

Creation of both MRI and CT templates have been created using the methods developed by Gabriel A. Devenyi (https://github.com/gdevenyi) available here : 
https://github.com/CoBrALab/optimized_antsMultivariateTemplateConstruction. This pipeline is a re-implementation of the ANTs template construction pipeline requiring ANTs for the primary commands, and running on our cluster facilities using qbatch (https://islande.hub.inrae.fr/infrastructure).

Using this methodology we developed : 
  1/ In vivo T1-weigthed brain template and its associated Grey Matter, White Matter and CSF probability maps dedicated to morphometrical analysis.
  2/ In vivo T2-weighted brain template with its FA and RGB template dedicated to diffusion analysis.
  3/ In vivo T1-weigthed brain template and its associated Grey Matter, White Matter and CSF probability maps dedicated to functional analysis.
  4/ In vivo CT head template and its associated head atlas of head cavities for cavities volume analysis.
  5/ Two brain atlas :  1. a brain atlas composed by mosaic of 115 regions of interest (ROI) covering the entire brain and built from a manual segmentation of subcortical regions and by a multi-animal dictionary learning statistical approach performed with Nilearn (https://nilearn.github.io/stable/index.html) applied to the functional data for the segmentation of the cortical areas. 
                        2. a fiber brain atlas composed by the 13 major bundles tracts of the equine brain created from the methods developped by C. Poupon (CEA, Neurospin, BAOBAB Team, https://joliot.cea.fr/drf/joliot/en/research/NeuroSpin/baobab) available at https://framagit.org/cpoupon/gkg. Atlas could be visualize using the anatomist from BrainVisa (https://brainvisa.info/web/)

## Organisation of the TEBTA resources

The TEBTA resources have been organized as five main sections : anatomy, functional, diffusion, computed tomography (CT), atlas.

  ### Anatomical Imaging
In this section, a set of templates, priors and brain mask is provivded for spatial normalization and analysis of anatomical MRI data dedicated to the equine brain.

T1-weighted template + associated probabilistics maps (GM, WM, CSF) + brain mask.
  
  Spatial resolution 0.8x0.8x0.8mm.
  
      t1.nii.gz
      prob01.nii.gz
      prob02.nii.gz
      prob03.nii.gz
      mask.nii.gz

  ### Functional Imaging
In this section, a set of templates, priors and brain mask is provivded for spatial normalization and analysis of functional MRI data dedicated to the equine brain.

T1-weighted template + associated probabilistics maps (GM, WM, CSF) + brain mask.

  Spatial resolution 1.6x1.6x1.6mm.
  
      t1.nii.gz
      prob01.nii.gz
      prob02.nii.gz
      prob03.nii.gz
      mask.nii.gz

  ### Diffusion Imaging
In this section, a set of templates, priors and brain mask is provivded for spatial normalization and analysis of diffusion MRI data dedicated to the equine brain.

T2-weighted template + fa template + RGB template + brain mask.

  Spatial resolution 2x2.4x2mm.
  
      t2.nii.gz
      rgb.nii.gz
      fa.nii.gz
      mask.nii.gz

  ### Computed Tomography Imaging (CT)
In this section a template and an atlas of head is provivded for spatial normalization and analysis of CT data and list of 8 labels created in ITKSnap Format

CT template + atlas + labels.

  Spatial resolution 1x1x1mm.
  
      ct.nii.gz
      atlas.nii.gz
      labels.nii.gz

  ### Brain Atlases (CT)
In this section, an atlas of the equine brain is provivded with a list of 115 labels created in ITKSnap Format.

Additionally, a fiber brain atlas is available in "dwi-equine-fiber-atlas" folder.

  Spatial resolution 0.8x0.8x0.8mm.
  
      atlas_labels.txt
      atlas.nii.gz
      dwi-equine-fiber-atlas/dwi-equine-brain.gii
      dwi-equine-fiber-atlas/dwi-equine-fiber-atlas.bundles
      dwi-equine-fiber-atlas/dwi-equine-fiber-atlas.bundlesdata
      dwi-equine-fiber-atlas/dwi-equine-fiber-atlas.hie

## Important Note
TEBTA ressources are provided at the scanner resolution and are oriented in anterior commisure/posterior commisure axis. Center of the images have been set at the anterior commisure level (Bregma 0 mm).

For any questions regarding the TEBTA ressource, please email David A. Barrière (david.barriere@cnrs.fr).

# REFERENCES
Valenchon M et al 2024 is currently under review (01/03/2024).
