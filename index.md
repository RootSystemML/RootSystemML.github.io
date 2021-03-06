---
title: RootSystemML home page
layout: default
---

[![RSML interoperability](/images/rsml_logo.png)](/images/interoperability.png)


RootSystemML is a file format to represent root architectural data. It has been designed to overcome two major challenges: 

 1. To enable portability of root architecture data between different software tools in an easy and interoperable manner allowing seamless collaborative work, 
 2. To provide a standard format upon which to base central repositories which will soon arise following the expanding worldwide root phenotyping effort.

RSML allows to store 2D or 3D image metadata, plant and root properties and geometries, continuous functions along individual root paths and a suite of annotations at the image, plant or root scales, at one or several time points. The plant ontologies are used to describe botanical entities that are relevant at the scale of root system architecture. 

##### The file format
RSML is based on the XML standard. It can store:

 - 2D or 3D image metadata
 - Plant and root properties and geometries
 - Continuous functions along individual root paths
 - A suite of annotations at the image, plant or root scales
 - All at one or several time points

An xml-schema-definition (xsd) can be used to validate the validity of an RSML file.

See [the file format page](format) for a detailed description of the features and constraints of RSML. 

##### Examples
[The examples page](examples) provides some RSML files and the images they have been constructed from. 

##### Supported software
The RSML format has been implemented in the following software:

1. Image analysis
  - [SmartRoot](http://smartroot.github.io)
  - [RootNav](http://www.cpib.ac.uk/tools-resources/software/rootnav/)
  - [RhizoScan](https://team.inria.fr/virtualplants/research/project/rhizoscan/)
  - [Root System Analyser](http://www.csc.univie.ac.at/rootbox/rsa.html)
  - [RooTrak](http://www.rootrak.net)
  - [EZ-Rhizo](mailto:adrian.hills@glasgow.ac.uk)
  - [GLO-RIA](http://www.rrlab.org/GLO-Roots/)

2. Modelling 
  - [RootBox](http://www.csc.univie.ac.at/rootbox)
  - [CRootBox](https://plant-root-soil-interactions-modelling.github.io/CRootBox/)
  - [SimRoot](http://rootmodels.gitlab.io/)
  - [R-SWMS](http://sites.uclouvain.be/RSWMS/)
  - ArchiSimple

3. Data analysis
  - [rsml for R](http://cran.r-project.org/web/packages/rsml/index.html)
  - [rsml for Excel](http://sourceforge.net/p/rootnav/code/ci/default/tree/)
  - [rsml for ImageJ](https://github.com/RootSystemML/RSML-conversion-tools/tree/master/imagej)
  - [rsml for Python](https://github.com/RootSystemML/RSML-conversion-tools/tree/master/python/rsml)
  - [ArchiDART](http://cran.r-project.org/web/packages/archiDART/index.html)

[comment]: # ([See the supporting software page for more details](software))

##### People
The RSML format was born from a collaboration between:

 - [Julien Diener](http://home-juliendiener.rhcloud.com/), INRIA, Virtual Plants
 - [Xavier Draye](http://www.uclouvain.be/xavier.draye), Université catholique de Louvain
 - [Christophe Godin](https://team.inria.fr/virtualplants/christophe-godin/), INRIA, Virtual Plants
 - [Daniel Leitner](mailto:daniel.leitner@univie.ac.at), University of Vienna
 - [Guillaume Lobet](http://www.guillaumelobet.be), Université de Liège
 - [Philipe Nacry](mailto:nacry@supagro.inra.fr), INRA
 - [Mike Pound](http://www.cpib.ac.uk/people/michael-pound/), University of Nottingham
 - [Christophe Pradal](https://team.inria.fr/virtualplants/christophe-pradal/), CIRAD, Virtual Plants
 - [Tony Pridmore](http://www.cpib.ac.uk/people/tony-pridmore/), University of Nottingham
 - [Andrea Schnepf](http://www.fz-juelich.de/ibg/ibg-3/EN/Staff/S/Schnepf%20Dr.%20Andrea.html?nn=1239630), Forschungszentrum Juelich 
