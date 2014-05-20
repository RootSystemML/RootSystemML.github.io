---
title: Standard format for RSA
layout: default
---

##The RSML file format

This page will describe the RootSystemML file format


#####Versioning
  - Upon publication the agreed format will be version 1.0. Any additional versioning will be agreed upon by all software developers, since all software will be required to handle the changes
  - All changes should be backwards compatible, unless a conversion tool is released.

#####General
  - The operation of software encountering optional values that it does not use (e.g z values in a 2D software program) is not defined. That is, it may ignore this data or attempt to use it, this is left to the discretion of the developer.
  - All information supplied in the file format should be preserved upon re-saving. This includes all function and annotation data, regardless of whether the saving software understands these. The only exceptions are mentioned as necessary below.
#####Metadata
  - File-key provides a position for a text representation of this file. Use of this field is left to the user’s discretion, we recommend it is used as a unique identifier.
  - All geometry and values within the document use the pixel as the unit of measurement, with the assumption that they refer directly to some underlying image data.
  - The unit tag specifies what units the resolution tag converts to, with the resolution tag detailing the conversion rate between pixels and the unit.
#####Property Definitions
  - These allow a given file to define types that will be used in the properties tags later in the document. For example, in the format “name type” the property “dead boolean" allows the <dead>true</dead> attribute to be added to the attributes tag for a plant or root.
  - The optional default tag can be used to provide a value where a tag is not found.
  - Software is not compelled to act on attributes found, they should be resaved.
  - The RSML specification provides a recommended list of pre-defined properties. Software should handle and use these properties whenever possible, and define only new and distinct properties.
#####Time Sequences
  - Label identifies an image as being part of a specific time sequence. Other documents in the same sequence must have the same label
  - Index identifies the position in the sequence relative to all other images with that label. Indexes should be unique within a sequence, and in ascending order relative to time captured.
  - Unified is a Boolean value indicating whether corresponding components share the same ids across files in the time sequence.
  - As a Boolean value, unified can be recorded as <unified>true</unified> and <unified>false</unified>. In the absence of a unified tag, the default value of false will be assigned.
#####Image Metadata
  - name specifies the file name of the image used to construct this root system. The name can be an absolute or relative url, or simply a file, but it should not be assume that this name refers to an existing file on a machine other than the original one.
  - sha256 specifies the hash of the entire image file using the SHA-256 hashing algorithm. This file fingerprint represents a more reliable means to locate the original source image, for example if it was stored in a database. The hash is calculated over the entire image file, including any header, palette or encoding information. The hash is not calculated over only the pixel data, as implementations may differ once the file is loaded. If the image is altered in any way the hash will change, this is the expected consequence.
  - Captured is a dateTime value indicating the original time of capture for that image. The ISO8601 should be followed: 2014-02-20  or  2014-02-20T14:44
#####Properties
  - The properties tags found within scene, plant and root tags represent the application of the property-definitions defined above. These can be used at the discretion of the software that produced the document. Other software is not expected to use these attributes, although it can.
  - Properties are semantically linked to the node in which they are found. For example, scene properties can be expected to relate to all plants in the scene.
  - Plant and Root Attributes
  - Two pre-defined attributes of label and ID exist that should be understood by all software. The label is the semantic name given to a specific root in some software, the ID represents a unique identifier for that root or plant.
  - Both ID and label are optional, IDs should be generated automatically as necessary where they are not included.
  - The po:accession attribute links to the plant ontology. They are expected to be of the form PO:$$$$$$$ where $ represents a single digit.
#####Geometry
  - The geometry node within a root represents the actual shape data, and represents the separation between topology (the nested structure of the root system defined through the XML structure) and geometry (the actual shape and size of each root).
  - Within the geometry tag, different geometry types can be defined at the discretion of the software. For example a spline tag, or a cylinder tag.
  - The polyline tag is mandatory, and represents the one geometry type guaranteed to be read and written by all software using this format.
  - Other geometry types are added in addition to, not instead of, the polyline
  - Being defined in the image domain, each point on the polyline contains mandatory x and y values, and an optional z value for 3D data.
#####Functions
  - Functions represent data attached directly to a polyline geometry. For example the amount of root hair along the length of a root.
  - There are three domains in which a function can be defined, these all directly map to the polyline geometry:
  - The ‘polyline’ domain defines a series of discrete samples along the length of a root. Each sample lies directly on the corresponding point in the geometry. If there are less samples than points on the geometry, then the latter points of the geometry are assigned no value. If there are more samples than points on the geometry, the latter samples are unused and may be discarded
  - The ‘uniform’ domain represents a series of uniformly distributed samples along the length of a root, where the position 0 is the origin of the root, and the position 1 is the opposite end. The root is still defined by the polyline geometry, being the only geometry guaranteed to exist. The first sample is always attached to position 0, the last sample to position 1. Other samples are spread evenly along the root length. For example, a function with 6 samples will be assigned the positions 0 0.2 0.4 0.6 0.8 1 in order. The attribute “origin” defines whether the origin is a root tip or base. 
  - The ‘length’ domain represents samples at specific length positions along a root, again on the polyline. Each sample provides a value and a position, with the position representing the pixel length along the root. Interpolation and extrapolation of unsampled regions of root material is left to each specific software implementation.
  - Software is expected to preserve all function data associated with a root in the event of resaving a file. This includes functions for which the software has no known mode of operation. The only exception is the exclusion below.
  - Functions are defined strictly over the polyline geometry. Any change to this geometry (position, number of points etc.) will invalidate all functions associated with this root. Software may re-calculate this information at its discretion, but otherwise this information should be discarded.
#####Annotations
  - Annotations represent semantic information added by the user.
  - While functions are defined over the polyline geometry of a root, annotations are attached to a topological object, e.g. a root, but are positioned in the image domain.
  - Annotation tags may appear in the scene, plant or root tags.
  - Annotations contain one pixel position representing the position of the value, and the value containing the actual annotation. Optional additional points can be added by software to represent a polygon to which the annotation applies. Other software is not required to use these additional points, but it should be saved.
  - In the case of 3D annotations, the point list represents the convex hull of the region associated with the annotation
  - As noted above, all annotation data is preserved upon saving the file. The only exception is where a plant or root has been removed from the file, thus associated annotation is also removed.
#####Time Series
  - Individual RSML files describe a root architecture at a given time step. Geometries are not explicitly related to those in a previous or subsequent time step. Except where the metadata contains a unified value of true.


[Back to RSML home](index)
