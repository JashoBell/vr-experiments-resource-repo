# VR Research Resource Repository

This repository is intended to be a curated repository of resources that are relevant to developing XR-based studies for experimental psychology or similar fields of research. Where possible, it is focused on free and open-source resources. If relevant, the resources should be actively maintained/updated, because this space moves relatively quickly and the changes tend to be substantive. It is not intended to be a list of all VR-related resources, but high-quality general resources that might be useful to VR experiments will be included. The goal is to provide a centralized location for all of the tools available to VR researchers, so the time normally spent searching for them can instead be spent developing, and development decisions can be made with all the relevant info available. 

If you have any suggestions for additions, please feel free to open a discussion thread, issue or pull request (after checking CONTRIBUTING.md), or just reach out to the maintainer (@jashobell) via another platform. If you are building an experiment and would like to either ask for assistance or share your experiences, triumphs and frustrations, feel free to open a discussion.

**Planned Additions**:

- Hardware platforms/Tracking systems
- More content (esp. Unreal Engine)
- A wiki
    - Tutorials/Informational content
    - References
        - Guidelines/Best Practices (e.g. [Vasser & Aru, 2020](https://www.sciencedirect.com/science/article/pii/S2352250X20300683))
        - Exemplars

# Table of Contents
- [Platforms](#software-platforms)
- [Experimental Design](#experimental-design)
- [3D Environment Building](#3d-environment-building)
    - [Applications](#applications)
    - [Asset Collections](#asset-collections)
- [Avatars](#avatars)
- [Feature Development](#feature-development)
    - [Inverse Kinematics (IK) Solvers](#inverse-kinematics-ik-solvers)
    - [Data Collection](#data-collection)
    - [Movement Smoothing](#movement-smoothing)



## Software Platforms
These are the applications you might use to build your experiment. Platform constraints on assets/resources will be noted via a preceding emoji.

[PsychVRToolbox](http://psychtoolbox.org/docs/PsychVRToolbox) - A collection of functions for building VR experiments with MATLAB/GNU Octave.  
[PsychXR](psychxr.org) - A Python library for building VR experiments, could be considered a VR extension of [PsychoPy](https://www.psychopy.org/) (and uses PsychoPy for rendering).  
:green_circle: [Unity](https://unity.com/) - A free cross-platform engine focused on game development but capable of VR experiments. *Note:* Requires a free Unity account to use.  
:orange_square: [Unreal Engine](https://www.unrealengine.com/en-US) - A free and open-source cross-platform engine focused on game development, but also able to be used for VR experiments. *Note:* Requires a free Epic Games account to use.
:large_blue_diamond: [Vizard](https://www.worldviz.com/vizard-virtual-reality-software) - A VR application development platform focused on professional use that leverages Python as its scripting language. *Note:* Closed source, license fee involved.    
:white_large_square: Platform-agnostic/Multiplatform  


## Experimental Design

### Frameworks
This section covers experimental "frameworks", or libraries that simplify the essential processes of conducting a behavioral experiment.

- :green_circle: [BioMotionLab Toolkit (Bebko & Troje, 2020)](https://github.com/BioMotionLab/TUX) - An framework for building experiments in Unity, aimed at reducing the amount of code needed to bring your design into practice ([Article](https://psyarxiv.com/arvkf/)).    
- :green_circle: [Mixed Reality - Remote Immersive Experiment Workflows (MR-RIEW; Bovo et al., 2022)](https://github.com/CrowdVRLab/MR-RIEW) - A toolkit for virtual and augmented reality that provides researchers with a dynamic way to design an immersive experiment workflow including instructions, environments, sessions, trials and questionnaires [Paper](https://ieeexplore.ieee.org/document/9757432).
- :green_circle: [Unity Experiment Framework (UXF; Brookes et al., 2019)](https://github.com/immersivecognition/unity-experiment-framework) - A set of components which simplify human behaviour experiments developed in the Unity engine. Includes a tutorial ([Article](https://link.springer.com/article/10.3758/s13428-019-01242-0)).
- :green_circle: [Ubiq-Exp](https://ubiq.online/publications/ubiq-exp/): A set of tools and examples that extends the [Ubiq](https://github.com/UCL-VR/ubiq/) system to support distributed and remote MR experiments (Note: Not publicly released as of 01/13/22; [Article](https://www.frontiersin.org/articles/10.3389/frvir.2022.912078/full)).
- :green_circle: [Unified Suite for Experiments (USE; Watson et al., 2019)](http://accl.psy.vanderbilt.edu/resources/analysis-tools/unifiedsuiteforexperiments/) - "a software and hardware solution for the development, management, and analysis of dynamic, video-game-like behavioral neuroscience experiments", uses a custom Arduino-based Synchbox to synchronize multiple hardware peripherals ([Article](https://www.sciencedirect.com/science/article/abs/pii/S0165027019302316)).
- :large_blue_diamond: [vexptoolbox (Schuetz et al., 2022)](https://github.com/ischtz/vizard-experiment-toolbox) - A software toolbox for human behavior studies using the Vizard virtual reality platform ([Article](https://link.springer.com/article/10.3758/s13428-022-01831-6)).

### Data Collection
These resources augment the experimental design frameworks above with additional features for data collection.

- :green_circle: [Rapid Sampling for Unity Experiments](https://github.com/JashoBell/rapid-sampling-for-unity-experiments) - Some custom UXF-based tracking scripts that use multithreading to sample motion data from a variety of tracking sources at a higher rate than Unity's framerate cap (currently, OpenVR and VRPN).
- :green_circle: [VRQuestionnaireToolkit](https://github.com/MartinFk/VRQuestionnaireToolkit) - A Unity toolkit for building and presenting questionnaires in VR ([Paper](https://hcitang.org/papers/2020-uist2020wip-feick-vrqt.pdf)).

## 3D Environment Development
This section is primarily focused on the creation of realistic 3D environments for VR experiments.

### Applications
- :white_large_square: [Blender](https://www.blender.org/) - A free and open-source 3D creation suite.  
    - (Recommended Add-on) [Archimesh](https://docs.blender.org/manual/en/3.3/addons/add_mesh/archimesh.html) - Easy generation of rooms, doors, windows and some objects.
- :white_large_square: [Materialize](https://boundingboxsoftware.com/materialize/) - A free and open-source application that allows you to create seamless tiles and texture maps from a single image.

### Asset Collections
- :white_large_square: [AmbientCG](https://ambientcg.com/) - A collection of high-quality CC0 assets, including textures, models, and HDRIs. Many textures are procedurally generated with Substance Designer.
- :white_large_square: [Polyhaven](https://polyhaven.com/) - A collection of high-quality CC0 assets, including textures, models, and HDRIs. Most textures are based on photographs.
- :white_large_square: [Sketchfab](https://sketchfab.com/) - A collection of assets varying in quality, licensing status, and price. Many assets are CC0, and many others are free to use in non-commercial settings with attribution.
    - [1702+ Photogrammetry-based Animal/Plant Models](https://sketchfab.com/ffishAsia-and-floraZia) - Massive collection of models based on photogrammetry scans of animals and plants. CC-BY Non-commercial.
- :white_large_square: [Textures.com](https://www.textures.com/) - A collection of high-quality 3D assets. A limited number of free downloads each day with an account, but assets are not redistributable.

### Standardized Assets
- :white_large_square: [OpenVirtualObjects (Tromp et al., 2020)](https://edmond.mpdl.mpg.de/dataset.xhtml?persistentId=doi:10.17617/3.ANGZTW) - 124 realistic 3D models of commonly-used and encountered household objects, rated "for recognizability, familiarity, details (i.e., visual complexity), contact, and usage (i.e., frequency of usage in daily life)" by adult participants ([Article](https://www.frontiersin.org/articles/10.3389/frvir.2020.611091/full)).
- :white_large_square: [Standardized Set of 3D Objects (Peeters, 2017)](https://archive.mpi.nl/mpi/islandora/object/mpi:1839_CA8BDA0E_B042_417F_8661_8810B57E6732?asOfDateTime=2018-03-02T11:00:00.000Z) - 147 objects belonging to "several different semantic categories, including food items, furniture, clothing, toys, and vehicles". Objects "have been normed for name agreement, image agreement, familiarity, visual complexity, and corresponding lexical characteristics of the modal object names" ([Article](https://link.springer.com/article/10.3758/s13428-017-0925-3)).

## Avatars
- :green_circle: :orange_square: [Microsoft Rocketbox (Gonzalez-Franco et al., 2020)](https://github.com/microsoft/Microsoft-Rocketbox) - A large and relatively diverse collection of characters and avatars released under the MIT license, including children and animals. Avatars are rigged with Mixamo animations and facial blendshapes [Article](https://www.frontiersin.org/articles/10.3389/frvir.2020.561558/full). 
    - Note: If you intend to use them as self-avatars in Unity, see this [pull request](https://github.com/microsoft/Microsoft-Rocketbox/pull/19) that fixes an issue with the avatar's construction on import.
    - (Relevant Utility) [Movebox](https://github.com/microsoft/MoveBox-for-Microsoft-Rocketbox) - A toolbox for animating the rocketbox avatars.
- :green_circle: :orange_square: [Mixamo](https://www.mixamo.com/) - A collection of humanoid models with animations. Also a system for adding animations to your own models.

## Feature Development  
Third-party libraries and tools that can be used to implement features in your VR experiment.

### General

- :green_circle: :orange_square: [Mixed Reality Toolkit](https://github.com/microsoft/MixedRealityToolkit) - "MRTK is a Microsoft-driven project that provides a set of components and features, used to accelerate cross-platform MR app development in Unity or Unreal". 
- :green_circle: [QuickVR (Oliva et al., 2022)](https://github.com/eventlab-projects/com.quickvr.quickbase) - A Unity library aimed at simplifying the integration of several VR features, with a focus on VR embodiment and avatar-related functionality (e.g. inverse kinematics; [Article](https://www.frontiersin.org/articles/10.3389/frvir.2022.937191/full)).

### Inverse Kinematics (IK) Solvers
These resources enable the implementation of self-avatars for participants.

- :green_circle: [FinalIK](https://assetstore.unity.com/packages/tools/animation/final-ik-14290) - A paid asset (often on sale) for Unity that includes a variety of IK solvers. VRIK in particular is useful in this context, and implements full-body IK.
- :green_circle: :orange_square: [Manus Polygon](https://www.manus-meta.com/software/polygon) - Free full-body motion capture software that can stream data into Unity or Unreal. Does not facilitate partial IK (i.e., you need enough trackers attached for full-body tracking).
- :green_circle: [VRArmIK (Parger et al., 2018)](https://github.com/dabeschte/VRArmIK) - IK solver focused on recreating arm movements from the head and hand. Useful for implementing a self-avatar with only a head-mounted tracker and a hand tracker ([Abstract](https://dl.acm.org/doi/abs/10.1145/3281505.3281529)).

### Movement Smoothing
These resources can be used to smooth positional data in real-time. Useful if representing virtual objects with potentially noisy motion capture data (e.g., Infrared LED) that don't otherwise implement smoothing.

- :green_circle: [OneEuro Filter (Unity Implementation)](https://github.com/DarioMazzanti/OneEuroFilterUnity) - A port of the [OneEuro](https://gery.casiez.net/1euro/) filter to Unity.
