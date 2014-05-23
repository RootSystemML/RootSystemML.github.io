---
title: RSML Thesaurus
layout: default
---


####RSML Thesaurus

RSML allows any property to be defined. However, the *RSML thesaurus* provides a list of standardized property which are recommended for use.

This list is not static and new entries can be added by the member of the [RootSystemML github organization][RSML org]. However, its content needs not be implemented by RSML software.

[RSML org]: https://github.com/RootSystemML

The following rhesaurus entries follows the format:

######name: (scale it applies to)
Description
 - possible value: meaning
 - possible value
 - ...

#####Property thesaurus:

######complete: (root)
Indicates if the root axes has been fully traced ([unit][]: string)

 - “yes”: it is fully traced (from parent to tip)
 - “no”: only a part of the axes has been traced
 
######branch-list: (root)
Indicates which sub-axes have been traced ([unit][]: string)

 - “complete”: root children branch have all been traced
 - “validated”: complete and it has been validated by the user
 - “random”: a random sample has been traced
 - “stratified”: a selected sample, representative of the roots type and density, has been traced
 
######category:
Gives a sub category of the selected plant ontology ([unit][]: string)
 - (Example for lateral root): “fine”, “long”
 
######branch-count: (root)
Independent count of the number of branches ([unit][]: integer)

######parent-node: (root)
This property allows for to connect the root axes to the parent axes. More precisely, it indicates which node of the parent axe the first node of this axe is. ([unit][]: integer)
 - Eg: “3” means the first node is the same as the 3rd node of parent axe
 
######parent-position: (root)
Indicates at which position on the parent axe this axe starts ([unit][]: real)
 - Eg: "3.2" means 20% between the 3rd and 4th nodes in parent polyline

######User-confidence: (scene, plant and root)
Indicates the confidence on the measured axe polyline ([unit][]: string or real)
 - high
 - medium
 - low
 - invalid
 - software-confidence: (at scene, plant or root)
 - A value in [0,1]: trust in the tracing, 1 is highest trust
 
#####Function thesaurus:

######confidence:
confidence in the root node position or other measurements such as diameter ([unit][]: real)
 - A values in \[0,1\]: (1 highest trust) for all node of the polyline

[unit]: format/units