# The Turone Equine Brain Templates and Atlases

The current document is a short description of the first version of the Turone Horse Brain Templates and Atlases resources (THBTA) dedicated to equine brain MRI data analysis. 
For a full description of the resources and the methodologies used to create them please consult the main publication [Valenchon M et al 2024].

The THBTA resources are a set of standardized MRI and CT compatible templates and atlases meant to support the analysis of multimodal MRI data of the equine brain. 
They were developped as part of the EQUISOBRAIN project, funded by the european Marie Skłodowska-Curie Actions (MSCA) program (Number: 101033271) and the Institut Français du Cheval et de l'Equitation.
THBTA provide a unified and standardized framework for the analysis of multimodal equine brain imaging data, allowing the reporting of results within the a sterotaxic coordinate system.

MRI and CT compatible in-vivo templates have been built from 23 horses (12 females and 11 males) 1-years old using a 3T scanner (Siemens Verio) onto the PIXANIM Imaging plateform (https://eng-pixanim.val-de-loire.hub.inrae.fr/).

Creation of both MRI and CT templates have been created using the methods developed by Gabriel A. Devenyi (https://github.com/gdevenyi) available here : 
https://github.com/CoBrALab/optimized_antsMultivariateTemplateConstruction. This pipeline is a re-implementation of the ANTs template construction pipeline requiring ANTs for the primary commands, and running on our cluster facilities using qbatch (https://islande.hub.inrae.fr/infrastructure).

Using this methodology we devopped : 
  1/ In vivo T1- and T2-weigthed brain templates and their associated Grey Matter, White Matter and CSF probability maps of the horses brain.
  2/ 

## Organisation of the THBTA resources

The THBTA resources have been organized as 

  ### Head templates
