# EuroPOND software tools

This repository contains software tools for modeling progression of diseases, developed within the [EuroPOND](http://www.europond.eu) project (European Progression of Neurological Diseases, funded by the European Union’s Horizon 2020 research and innovation programme under grant agreement No. 666992).

These software tools allow building scenarios of disease progression, studying their variability and heterogeneity within populations and staging of individual patients. They take as inputs various types of medical measurements (clinical/cognitive scores, biomarker measurement, medical images, anatomical shapes...). While mainly developed for neurological diseases, they are potentially applicable to other disorders.

## EBM (event-based model)
**TODO (@UCL): add description, if possible following the same organization used for Leasp**

## pyEBM
**TODO (@EMC): add description, if possible following the same organization used for Leasp**

## Leasp (LEArning Spatiotemporal Patterns)
![imageLeasp](./images/leasp_800.jpg)
- **Leasp** is a software tool for estimating models of progression from longitudinal measurements.
- **Examples of applications in neurological diseases:** learning trajectories of progression for clinical/cognitive scores, fluid biomarker measurements (e.g. CSF, blood), volumetric MRI measures, other regional neuroimaging measures (e.g. FDG PET, Amyloid PET), cortical thickness maps   
- **Links**
  - [Repository](https://gitlab.icm-institute.org/aramislab/longitudina)
  - [Documentation](https://gitlab.icm-institute.org/aramislab/longitudina/blob/master/README.md)
- **Type of inputs:** longitudinal scalar measurements (e.g. clinical/cognitive scores, biomarker measurements) or network-valued measurements (e.g. cortical thickness map)
- **Related publications**
  - **Generic model** - Jean-Baptiste Schiratti, Stéphanie Allassonnière, Olivier Colliot, and Stanley Durrleman. A Bayesian mixed-effects model to learn trajectories of changes from repeated manifold-valued observations.
*The Journal of Machine Learning Research*, 18:1–33, December 2017. [Open Access PDF](https:
//hal.archives-ouvertes.fr/hal-01540367).
  - **Model for network-valued measurements** - Igor Koval, Jean-Baptiste Schiratti, Alexandre Routier, Michael Bacci, Olivier Colliot, Stéphanie Allassonnière, and Stanley Durrleman. Spatiotemporal Propagation of the Cortical Atrophy: Population and Individual Patterns. *Front Neurol.* 2018 May 4;9:235. [Open Access PDF](https://www.frontiersin.org/articles/10.3389/fneur.2018.00235/full).

- **Description.** This software package implements a generic Bayesian mixed-effects model to estimate the temporal progression of a biological phenomenon from observations obtained at multiple time points for a group of individuals. The progression is modeled by continuous trajectories in the space of measurements. Individual trajectories of progression result from spatiotemporal transformations of an average trajectory. These transformations allow to quantify the changes in direction and pace at which the trajectories are followed. The framework of Riemannian geometry allows the model to be used with any kind of measurements with smooth constraints. A stochastic version of the Expectation-Maximization algorithm is used to produce produce maximum a posteriori estimates of the parameters.

## Deformetrica
![imageDeformetrica](./images/deformetrica_800.jpg)
- Models of progression from longitudinal shape or image data are implemented in the **Deformetrica** software package. Deformetrica also implements various other functionalities for statistics on shapes and images, including registration, atlas construction and geodesic regression.
- **Type of inputs:** longitudinal shapes or images (e.g. meshes of anatomical structures)
- **Examples of applications in neurological diseases:** learning trajectories of atrophy of anatomical shapes (e.g. hippocampal shape extracted from anatomical MRI)
- **Links**
  - [Website](http://www.deformetrica.org/)
  - [Repository](https://gitlab.icm-institute.org/aramislab/deformetrica)
  - [Documentation](https://gitlab.icm-institute.org/aramislab/deformetrica/wikis/home)
- **Related publications**
  - **Model for longitudinal shape data** - Alexandre Bône, Olivier Colliot, and Stanley Durrleman. Learning distributions of shape trajectories
from longitudinal datasets: a hierarchical model on a manifold of diffeomorphisms. *In CVPR 2018 - Computer Vision and Pattern Recognition 2018*, Salt Lake City, United States, June 2018. [Open Access PDF](https://hal.archives-ouvertes.fr/hal-01744538).
  - **Generic description of Deformetrica** - Alexandre Bône, Maxime Louis, Benoît Martin, Stanley Durrleman, Deformetrica 4: an open-source software for statistical shape analysis, *In Proc ShapeMI Workshop, MICCAI 2018*, Sep 2018, Granada, Spain [Open Access PDF](https://hal.inria.fr/hal-01874752v2).
- **Description.** The implemented approach allows to learn a distribution of shape trajectories from longitudinal data, i.e. the collection of individual objects repeatedly observed at multiple time-points. It can in particuler be applied to any series of anatomical shapes (represented as meshes) extracted from medical images. The method allows to compute an average spatiotemporal trajectory of shape changes at the group level, and the individual variations of this trajectory both in terms of geometry and time dynamics. The model is formulated as the combination of a generic statistical model for manifold-valued longitudinal data, a deformation model defining shape trajectories via the action of a set of diffeomorphisms with a manifold structure, and an efficient numerical scheme to compute parallel transport on this manifold.

## DEM
**TODO (@UCL): add description, if possible following the same organization used for Leasp**`

## SuStaIn
**TODO (@UCL): add description, if possible following the same organization used for Leasp**`

## DIVE
**TODO (@UCL): add description, if possible following the same organization used for Leasp**`

## Gaussian process regression models
**TODO (@UCL): add description, if possible following the same organization used for Leasp**`

## Clinica
![imageDeformetrica](./images/clinica_800.jpg)
- **Clinica** allows extracting measurements (volumetric and other regional measures, voxel-based maps, cortical thickness, meshes...) from brain imaging data. It also allows converting public datasets (ADNI, AIBL, OASIS) into the standard community format BIDS.
- **Type of inputs:** neuroimaging data (anatomical MRI, diffusion MRI, PET).
- **Examples of applications:** extracting measurements that can then be used as inputs of disease progression modeling software (e.g [EBM](EBM), [pyEBM](pyEBM), [Leasp](Leasp), [Deformetrica](Deformetrica)...)
- **Links**
  - [Website](http://www.clinica.run/)
  - [Repository](https://gitlab.icm-institute.org/aramislab/clinica)
  - [Documentation](http://www.clinica.run/doc/)
- **Related publications**
  - **General presentation of Clinica software** - Alexandre Routier, Jérémy Guillon, Ninon Burgos, Jorge Samper-Gonzalez, Junhao Wen, Sabrina
Fontanella, Simona Bottani, Thomas Jacquemont, Arnaud Marcoux, Pietro Gori, Pascal Lu, Tristan Moreau, Michael Bacci, Stanley Durrleman, and Olivier Colliot. Clinica: an open source software
platform for reproducible clinical neuroscience studies. *In Annual meeting of the Organization for Human Brain Mapping - OHBM 2018*, Singapore, Singapore, June 2018. [Open Access PDF](https://hal.inria.fr/hal-01760658).
  - **T1 MRI and PET applications** - Jorge Samper-Gonzalez, Ninon Burgos, Simona Bottani, Sabrina Fontanella, Pascal Lu, Arnaud Marcoux,
Alexandre Routier, Jérémy Guillon, Michael Bacci, Junhao Wen, Anne Bertrand, Hugo Bertin, Marie-Odile Habert, Stanley Durrleman, Theodoros Evgeniou, and Olivier Colliot. Reproducible
evaluation of classification methods in Alzheimer’s disease: Framework and application to MRI and PET data. *NeuroImage*, 183:504–521, December 2018. [Open Access PDF](https://hal.inria.fr/hal-01858384).
- **Description.** Clinica is a software platform for multimodal brain image analysis in clinical research studies. It makes it easy to apply advanced analysis tools to large scale clinical studies. For that purpose, it integrates a comprehensive set of processing tools for the main neuroimaging modalities: currently MRI (anatomical, functional, diffusion) and PET, in the future, EEG/MEG.
For each modality, Clinica allows to easily extract various types of features (regional measures, parametric maps, surfaces, curves, networks). Such features are then subsequently used as input of machine learning, statistical modeling, morphometry or network analysis methods. Processing pipelines are based on combinations of freely available tools developed by the community. It provides an integrated data management specification to store raw and processing data. Clinica is written in Python. It uses the Nipype system for pipelining. It combines widely-used software for neuroimaging data analysis (SPM, Freesurfer, FSL, MRtrix...), morphometry (Deformetrica), machine learning (Scikit-learn) and the BIDS standard for data organization.
