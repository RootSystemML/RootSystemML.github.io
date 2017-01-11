---
title: RSML Thesaurus
layout: default
---


#### RSML Thesaurus

RSML allows any property or function to be defined. However, the *RSML thesaurus* provides a list of standardized property and function which are recommended for use. Also, those terms should be avoided if the function or property meaning is not as described here.

This thesaurus is not static and new entries can be added by the RSML format autors and the members of the [RootSystemML organization][RSML org] through the [indicated open-source protocol][new-entries]. However, the thesaurus content needs not be implemented by all RSML software.


[new-entries]: #adding-new-entry-to-the-thesaurus


________ 
The thesaurus entries follows the format:

###### name: (scales it applies to)
Description (property/function type)

 - possible value: meaning
 - other possible value
 - ...
 
________ 



##### Property thesaurus:


###### species: (scene,plant)
Indicate the plant species in the image. Use latin names

###### genotype: (scene,plant)
Indicate the plant genotype in the image.

###### medium: (scene)
Indicate the growing medium used for the plant present in the image. e.g. *agar*, *hoagland*, ...

###### treatment: (scene)
Indicate wether a specific treatment was applied to the plants. e.g. *water stress*, *mock*, *P deficiency*, ...

###### age_of_plant: (scene, plant)
Age of the plant, in days.

###### complete: (root)
Indicates if the root axes has been fully traced ([type][]: string)

 - “yes”: it is fully traced (from parent to tip)
 - “no”: only a part of the axes has been traced
 
###### branch-list: (root)
Indicates which sub-axes have been traced ([type][]: string)

 - “complete”: root children branch have all been traced
 - “validated”: complete and it has been validated by the user
 - “random”: a random sample has been traced
 - “stratified”: a selected sample, representative of the roots type and density, has been traced
 
###### category: (root)
Gives a sub category of the selected plant ontology ([type][]: string)

 - Eg (for lateral root): “fine”, “long”
 
###### branch-count: (root)
Independent count of the number of branches ([type][]: integer)

###### parent-node: (root)
This property allows **to connect** the root axes to the parent axes. More precisely, it indicates which node of the parent axe is actually the first node of this axe. ([type][]: integer)

 - Eg: “3” means this axe 1st node is the same as the 3rd node of parent axe
 
###### parent-position: (root)
Indicates at which position on the parent axe this axe starts. This preperty is to indicates a measured branching position along the parent root. It does not connect the axes. ([type][]: real)

 - Eg: "3.2" means 20% between the 3rd and 4th nodes in parent polyline

###### user-confidence: (scene, plant and root)
Indicates the confidence on the measured axe polyline given by user ([type][]: string)

 - high
 - medium
 - low
 - invalid

###### software-confidence: (scene, plant or root)
Indicates the confidence on the measured axe polyline given by (automated) software ([type][]: real)

 - A value in [0,1]: trust in the tracing, 1 been highest trust


________ 

##### Function thesaurus:

###### diameter:
This gives the recorded diameter at each node of the root polyline in pixel. ([type][]: real)

 - Positive values \[0,inf)

###### confidence:
confidence in the root node position of the polyline ([type][]: real)

 - A value in [0,1]: trust in the node postion, 1 been highest trust

###### xxxx-confidence:
confidence in the root property `xxxx` ([type][]: real)

 - A value in [0,1]: trust in the property value, 1 been highest trust


________ 

##### Adding new entry to the Thesaurus

The thesaurus reference text is this page. In order to add an entry, two methods are to be followed depending on RSML authorship and membership.

For the authors and [RootSystemML][RSML org] members, a dedicated [wiki page][] has been set to discuss possible addition.

For the others:

 1. Fork the [RSML website source][RSML_site_git]
 2. Make the requested addition in `format/thesaurus.md` 
 3. Do a pull request to merge the fork site describing its use and scope
 
Or you can contact one of the [RootSystemML][RSML org] members that you know to have him/her do the addition.

 
In both cases:

 - At least two members representing two different groups (i.e. software) should accept it
 - before acceptance, the members should inform all the RSML authors and let sufficient time for them to answer
 

[Back to RSML file format](index)
 
[type]: units
[wiki page]: https://github.com/RootSystemML/RootSystemML.github.io/wiki/Thesaurus
[RSML org]: https://github.com/RootSystemML
[RSML_site_git]: https://github.com/RootSystemML/RootSystemML.github.io

