---
title: RSML R package
layout: default
---

### Aim

The R package allow the import, analysis and plotting of RSML datafiles. 

The API is based on three new classes:

- **node**: lowest information level. Contains the actual coordinates of the different polylines contained in the RSML file. Cain contain morphological information such as the diameter, age, orientation of the nodes.
- **root**: collection of nodes formation a biological root. Can contain children. 
- **plant**: collection of roots forming the root system

These thre levels allows the user to easily retrieve data that are biologically relevant such as the total length of the different root types, the insertion angles or the 3D repartitions of the roots in space. 

**WARNING** : RSML-R is still in development, so miskakes can happen... If so, please contact [Guillaume Lobet](mailto:guillaume.lobet@ulg.ac.be)

### Use
    
    path <- "~/Desktop/Divers/rsml_tests/lupin-aero-1.rsml"
    
    # Get the RSML file as a table containing the root information
    pl.list <- rsmlToList(path)
    write.csv(pl.list$processed, "~/Desktop/rsml-table.csv")
    
    # Get the RSML as  a plant object
    pl <- rsmlToPlant(path)
    
    # Plot the plant
    plot(pl)
    
    # Display the plant properties
    print(pl)
    
    # Get the plant summary
    sum.plant <- summary(pl)
    sum.plant$total.length$value # Get the total lenght of the plant
    sum.plant$prim.length$value # Get the primary lenght of the plant
    
    # try to load 3D data
    data(anagallis)
    plot(anagallis, threed = T)
    print(anagallis)





[View source on GitHub](https://github.com/RootSystemML/RSML-conversion-tools/tree/master/r) | [Download binaries](https://github.com/RootSystemML/RSML-conversion-tools/blob/master/r/RSML_1.2.tgz)

[![R interface](/images/r_rsml.png)](/images/r_rsml.png)

## Other tools

[R](/tools/r_rsml) | [ImageJ](/tools/imagej_rsml) |  [Python](/tools/python_rsml) | [Excel](/tools/excell_rsml) | [C#](/tools/c_rsml) | [Back to RSML home](/index)

