---
title: Metadata of RSML
layout: default
---

####The RSML metadata

```
    <metadata>
        <version>1</version>
        <unit>pixel</unit>
        <resolution>1</resolution>
        <last-modified>2014-02-20T00:00:00</last-modified>
        <software>RSML-example</software>
        <user>RSML-team</user>
        <file-key>RSML-metadata-example</file-key>
        <image>
            <name>name_of_image_file</name>
            <captured>2014-02-19T00:00:00</captured>
            <sha256>XXXXXXXXX</sha256>
        </image>
    </metadata>
```

#####version
  - Upon publication the agreed format will be version 1.0. Any additional versioning will be agreed upon by all software developers, since all software will be required to handle the changes
  - All changes should be backwards compatible, unless a conversion tool is released.

#####resolution and unit
  - All geometry and values within the document use the pixel as the unit of measurement, with the assumption that they refer directly to some underlying [image data](#image).
  - The unit tag specifies what units the resolution tag converts to, with the resolution tag detailing the conversion rate between pixels and the unit. If possible, one of the [standard units][] should be used. 

[standard units]: units
  
#####last-modified
  - date and time stamp of the last modification of the rsml file
  - It should respect the [ISO8601][] format
  
#####file-key
  - File-key provides a position for a text representation of this file. Use of this field is left to the user’s discretion, we recommend it is used as a unique identifier.
  
#####image
  - **name** (mandatory) specifies the file name of the image used to construct this root system. The name can be an absolute or relative url, or simply a file, but it should not be assume that this name refers to an existing file on a machine other than the original one.
  - **captured** (optional) is a dateTime value indicating the original time of capture for that image. It should be given in  [ISO8601][] format
  - **sha256** (optional) specifies the hash of the entire image file using the [SHA-256][] hashing algorithm. This file fingerprint represents a more reliable means to locate the original source image, for example if it was stored in a database. The hash is calculated over the entire image file, including any header, palette or encoding information. The hash is not calculated over only the pixel data, as implementations may differ once the file is loaded. If the image is altered in any way the hash will change, this is the expected consequence.

[ISO8601]: units#data-and-time
[SHA-256]: http://en.wikipedia.org/wiki/SHA-2
  
#####property-definitions
  - These allow a given file to define types that will be used in the properties tags later in the document. For example, in the format “name type” the property “dead boolean" allows the `<dead>true</dead>` attribute to be added to the attributes tag for a plant or root.
  - The optional default tag can be used to provide a value where a tag is not found.
  - Software is not compelled to act on attributes found, they should be resaved.
  - The RSML specification provides a recommended list of pre-defined properties. Software should handle and use these properties whenever possible, and define only new and distinct properties.

#####Time Sequences
  - Label identifies an image as being part of a specific time sequence. Other documents in the same sequence must have the same label
  - Index identifies the position in the sequence relative to all other images with that label. Indexes should be unique within a sequence, and in ascending order relative to time captured.
  - Unified is a Boolean value indicating whether corresponding components share the same ids across files in the time sequence.
  - As a Boolean value, unified can be recorded as <unified>true</unified> and <unified>false</unified>. In the absence of a unified tag, the default value of false will be assigned.

[Back to RSML file format](index)


<!--
[test link to section in same page](#version)
[test link to section in same page](#resolution-and-unit)

[test link to section in other page](scene#annotations)
[test link to section in other page](scene#time-series)

conclusion:
 - one # followed by the section name, the section level is irrelevant
 - use lower-case section name and replace spaces by '-'
-->

