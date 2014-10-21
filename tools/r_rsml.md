---
title: RSML R package
layout: default
---

The R package allow the import, analysis and plotting of RSML datafiles.

The API is based on three new classes:

- **node**: lowest information level. Contains the actual coordinates of the different polylines contained in the RSML file. Cain contain morphological information such as the diameter, age, orientation of the nodes.
- **root**: collection of nodes formation a biological root. Can be contain children. 
- **plant**: collection of roots forming the root system

These thre levels allows the user to easily retrieve data that are biologically relevant such as the totla length of the different root types, the insertion angles or the 3D repartitions of the roots in space. 


[View source on GitHub](https://github.com/RootSystemML/RSML-conversion-tools/tree/master/r) | [Download binaries](https://github.com/RootSystemML/RSML-conversion-tools/blob/master/r/RSML_1.0.tgz)

[![R interface](/images/r_rsml.png)](/images/r_rsml.png)

[R](/tools/r_rsml) | [ImageJ](/tools/imagej_rsml) |  [Python](/tools/python_rsml) |  [Excell](/tools/excell_rsml) |  [Back to RSML home](/index)

