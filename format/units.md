---
title: Units and variable format in RSML
layout: default
---

#####Date and time

Several rsml metadata, such as the [last-modified](metadata#last-modified) and [image>captured](metadata#image), indicate date (or date-time) data. Those should respect one of the following two [ISO8601](http://en.wikipedia.org/wiki/ISO_8601) format:
  - for a date only, use `yyyy-mm-dd`format
  - for date and time, use `Yyyyy-mm-ddThh:mi:si`

  
#####Units

This section provides a list of *standard* units which are recommanded for use in the [metadata unit](metadata#resolution-and-unit) and [property-definitions](metadata#property-definitions).

Numbers:

  - `boolean`: False,false,True,true,0,1
  - `integer`: ...-1,0,1,...
  - `real`:    -3.141592, 2.71828182846
  - `string`
                        
Measurements:

  - `m`: meter
  - `cm`: centimeter
  - `mm`: millimeter
  - `um`: micrometer
  - `nm`: nanometer
  - `pixel`
     
  
[Back to RSML file format](index)

