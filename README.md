# VR Research Resource Repository

This repository is intended to be a curated list of resources that are relevant to developing XR-based studies for experimental psychology or similar fields of research. Where possible, it is focused on free, open-source and recently updated resources. It is not intended to be a list of all VR-related resources. If you have any suggestions for additions, please feel free to open an issue or pull request (after checking CONTRIBUTING.md), or just reach out via another platform. If you are building an experiment and would like to either ask for assistance or share your experiences, triumphs and frustrations, feel free to open a discussion.

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
These are the applications you might use to build your experiment. I've included as many resources for each platform as are known to me, but this is highly Unity-biased as that is where I have the most experience (and it seems to have the most attention from experimental psychology). Platform constraints will be noted via a preceding emoji.

:green_circle: [Unity](https://unity.com/)  
:orange_square: [Unreal Engine](https://www.unrealengine.com/en-US)  
:large_blue_diamond: [Vizard](https://www.worldviz.com/vizard-virtual-reality-software)
*Note:* Closed source, license fee involved.  
:white_large_square: Platform-agnostic  

## Experimental Design
This section covers experimental "frameworks", or libraries that simplify the essential processes of conducting a behavioral experiment.

- :green_circle: [BioMotionLab Toolkit](https://github.com/BioMotionLab/TUX) - An framework for building experiments in Unity, aimed at reducing the amount of code needed to bring your design into practice.    
- :green_circle: [Mixed Reality - Remote Immersive Experiment Workflows (MR-RIEW)](https://github.com/CrowdVRLab/MR-RIEW) - A toolkit for virtual and augmented reality that provides researchers with a dynamic way to design an immersive experiment workflow including instructions, environments, sessions, trials and questionnaires.
- :green_circle: [Unity Experiment Framework (UXF)](https://github.com/immersivecognition/unity-experiment-framework) - A set of components which simplify human behaviour experiments developed in the Unity engine.
- :green_circle: [Ubiq-Exp](https://www.frontiersin.org/articles/10.3389/frvir.2022.912078/full): A set of tools and examples that extends the [Ubiq](https://github.com/UCL-VR/ubiq/) system to support distributed and remote MR experiments.
- :large_blue_diamond: [vexptoolbox](https://link.springer.com/article/10.3758/s13428-022-01831-6) - A software toolbox for human behavior studies using the Vizard virtual reality platform (Article).

## 3D Environment Building
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
- :white_large_square: [OpenVirtualObjects (Tromp et al., 2020)](https://edmond.mpdl.mpg.de/dataset.xhtml?persistentId=doi:10.17617/3.ANGZTW) - 124 realistic 3D models of commonly-used and encountered household objects, rated "for recognizability, familiarity, details (i.e., visual complexity), contact, and usage (i.e., frequency of usage in daily life)" by adult participants ([Paper](https://www.frontiersin.org/articles/10.3389/frvir.2020.611091/full)).
- :white_large_square: [Standardized Set of 3D Objects (Peeters, 2017)](https://archive.mpi.nl/mpi/islandora/object/mpi:1839_CA8BDA0E_B042_417F_8661_8810B57E6732?asOfDateTime=2018-03-02T11:00:00.000Z) - 147 objects belonging to "several different semantic categories, including food items, furniture, clothing, toys, and vehicles". Objects "have been normed for name agreement, image agreement, familiarity, visual complexity, and corresponding lexical characteristics of the modal object names" ([Paper](https://link.springer.com/article/10.3758/s13428-017-0925-3)).

## Avatars
- :green_circle: :orange_square: [Microsoft Rocketbox](https://github.com/microsoft/Microsoft-Rocketbox) - A large and relatively diverse collection of characters and avatars released under the MIT license. 
    - Note: If you intend to use them as self-avatars in Unity, see this [pull request](https://github.com/microsoft/Microsoft-Rocketbox/pull/19) that fixes an issue with the avatar's construction on import.
    - (Relevant Utility) [Movebox](https://github.com/microsoft/MoveBox-for-Microsoft-Rocketbox) - A toolbox for animating the rocketbox avatars.
- :green_circle: :orange_square: [Mixamo](https://www.mixamo.com/) - A collection of characters and avatars.

## Feature Development  

### General

- :green_circle: :orange_square: [Mixed Reality Toolkit](https://github.com/microsoft/MixedRealityToolkit) - "MRTK is a Microsoft-driven project that provides a set of components and features, used to accelerate cross-platform MR app development in Unity or Unreal". 

### Inverse Kinematics (IK) Solvers
These resources enable the implementation of self-avatars for participants.

- :green_circle: [FinalIK](https://assetstore.unity.com/packages/tools/animation/final-ik-14290) - A paid asset (often on sale) for Unity that includes a variety of IK solvers. VRIK in particular is useful in this context, and implements full-body IK.
- :green_circle: :orange_square: [Manus Polygon](https://www.manus-meta.com/software/polygon) - Free full-body motion capture software that can stream data into Unity or Unreal. Does not facilitate partial IK (i.e., you need enough trackers attached for full-body tracking).
- :green_circle: [VRArmIK](https://github.com/dabeschte/VRArmIK) - IK solver focused on recreating arm movements from the head and hand.  

### Data Collection
These resources augment the experimental design frameworks above with additional features for data collection.

- :green_circle: [Rapid Sampling for Unity Experiments](https://github.com/JashoBell/rapid-sampling-for-unity-experiments) - Some custom UXF-based tracking scripts that use multithreading to sample motion data from a variety of tracking sources at a higher rate than Unity's framerate cap (currently, OpenVR and VRPN).
- :green_circle: [VRQuestionnaireToolkit](https://github.com/MartinFk/VRQuestionnaireToolkit) - A Unity toolkit for building and presenting questionnaires in VR.


### Movement Smoothing
These resources can be used to smooth positional data in real-time. Useful if representing virtual objects with potentially noisy motion capture data (e.g., Infrared LED) that don't otherwise implement smoothing.

- :green_circle: [OneEuro Filter (Unity Implementation)](https://github.com/DarioMazzanti/OneEuroFilterUnity) - A port of the [OneEuro](https://gery.casiez.net/1euro/) filter to Unity.
