---
title: C# API
layout: default
---

RootNav contains an API for efficient Reading and Writing of RSML files. The source code is contained within the RootNav solution, but can be easily used externally to RootNav.

The API is contained within the RootNav.Data assembly, and consists of these notable classes:

- **IO.RSML.RootReader**: Will read RSML files and directories into C# classes.
- **IO.RSML.RootWriter**: Will write existing C# classes into one or more RSML files.
- **SceneInfo**: Contains all necessary metadata for an RSML file. Contains one or more PlantInfo objects.
- **PlantInfo**: Contains all of the metadata required for an RSML plant node. May contain one or more RootInfo objects.
- **RootInfo**: Contains all of the metadata and geometry required for an RSML root node. May contain child RootInfo objects.

These classes allow quantitative traits to be calculated over root systems easily. The RootNav.Measurement assembly can also be used to calculate a number of pre-defined traits if required. 


[View source on SourceForge](https://sourceforge.net/p/rootnav/code/ci/default/tree/) | [Download binaries](http://sourceforge.net/projects/rootnav/files/RSML%20C%23%20x64.zip/download)

## Other tools

[R](/tools/r_rsml) | [ImageJ](/tools/imagej_rsml) |  [Python](/tools/python_rsml) |  [Excel](/tools/excell_rsml)|  [C#](/tools/c#_rsml) |  [Back to RSML home](/index)

