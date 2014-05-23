---
title: RSML Thesaurus
layout: default
---


####RSML Thesaurus

RSML allows any property or functions to be defined. However, the *RSML thesaurus* provides a list of standardized property and functions which are recommended for use. Also, those terms should be avoided if the function or property meaning is not as described here.

This thesaurus is not static and new entries can be added by the RSML format autors and the members of the [RootSystemML github organization][RSML org] through the [indicated open-source protocol][new-entries]. However, the thesaurus content needs not be implemented by all RSML software.


[new-entries]: #adding-new-entry-to-the-thesaurus


________ 
The thesaurus entries follows the format:

######name: (scales it applies to)
Description (unit)

 - possible value: meaning
 - possible value
 - ...
 
________ 



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
 
######category: (root)
Gives a sub category of the selected plant ontology ([unit][]: string)

 - Eg (for lateral root): “fine”, “long”
 
######branch-count: (root)
Independent count of the number of branches ([unit][]: integer)

######parent-node: (root)
This property allows **to connect** the root axes to the parent axes. More precisely, it indicates which node of the parent axe is actually the first node of this axe. ([unit][]: integer)

 - Eg: “3” means this axe 1st node is the same as the 3rd node of parent axe
 
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


 
#####Adding new entry to the Thesaurus

The thesaurus main text is (currently) this page. In order to add an entry, the two methods can be followed depending on the membership.

For the [RootSystemML][RSML org] members, a dedicated [wiki page][] has been set to discuss possible addition.

For the others:

 1. Fork of the [RSML website source][RSML_site_git]
 2. Make the asked addition in `format/thesaurus.md` 
 3. Make pull request to merge the fork content describing its use and scope
 
Or if you can contact one of the [RootSystemML][RSML org] members that you know to have him/her do the addition.

 
In both cases:

 - At least two members representing two different groups (i.e. software) should accept it
 - before acceptance, the members should inform all the RSML authors and let sufficient time for them to answer
 

 
[unit]: units
[wiki page]: https://github.com/RootSystemML/RootSystemML.github.io/wiki/Thesaurus
[RSML org]: https://github.com/RootSystemML
[RSML_site_git]: https://github.com/RootSystemML/RootSystemML.github.io

