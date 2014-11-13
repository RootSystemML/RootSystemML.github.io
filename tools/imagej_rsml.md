---
title: ImageJ plugin - RSML Reader
layout: default
---

# Aim
The RSML Reader plugin allows users to import a bunch of RSML datafiles and extract the needed information, either at the plant, root or node level. 

For programmers, the plugin includes a complete API that could be re-used for other projects. 

# Installation

- Download the RSML_reader.jar file (see below)
- copy the RSML_reader.jar file to the folder **/ImageJ/plugin**

# Use

- Launch ImageJ
- Open the plugin throught the menu **Plugins/RSML Reader**
- Choose the source folder containing your rsml files
- Click **Export result to table**
- Choose the type of export
- If you want to display the RSML tracing as an image stack, click **Display image**
 - Note: due to ImageJ memory limit, asking for the display of a large number of RSML files will cause the plugi to stop.
- Right click on the table and save it as an XLS file.


[View source on GitHub](https://github.com/RootSystemML/RSML-conversion-tools/tree/master/imagej) | [Download .jar file](https://github.com/RootSystemML/RSML-conversion-tools/blob/master/imagej/bin/RSML_reader.jar?raw=true)
 
[![ImageJ RSML Reader](/images/imagej_rsml.png)](/images/imagej_rsml.png)


 
[R](/tools/r_rsml) | [ImageJ](/tools/imagej_rsml) |  [Python](/tools/python_rsml) |  [Excel](/tools/excell_rsml) |[C#](/tools/c_rsml) |  [Back to RSML home](/index)

