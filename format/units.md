---
title: Units and variable format in RSML
layout: default
---

This section provides a list of *standard* units which are recommanded for use typically in the [metadata unit](metadata#resolution-and-unit) and [property-definitions](metadata#property-definitions).


#####Variable types:

  - `boolean`: false,true,0,1
  - `integer`: ...-1,0,1,...
  - `real`:    -3.141592, 2.71828182846
  - `string`
                        
#####Date and time

Several rsml metadata, such as the [last-modified][] and [image-captured][], indicate date (or date-time) data. Those should respect one of the following two [ISO8601][] format:

  - for a date only, use `yyyy-mm-dd`format
  - for date and time, use `yyyy-mm-ddThh:mi:si`

where `yyyy` is the year, `mm` is the month, `dd` is the day, `hh` is the hour (between 0 and 24), `mi` is the minutes, `si` is the second
  
[last-modified]: metadata#last-modified
[image-captured]: metadata#image
[ISO8601]: http://en.wikipedia.org/wiki/ISO_8601

#####Measurements:

  - `m`: meter
  - `cm`: centimeter
  - `mm`: millimeter
  - `um`: micrometer
  - `nm`: nanometer
  - `pixel`
     
  
[Back to RSML file format](index)

