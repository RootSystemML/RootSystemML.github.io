---
title: RSML Examples
layout: default
---

This page provides a set of example rsml files as well as the images the root architecture has been constructed from.

RSML allows to store a variety of content. The basic data contained in an RSML file is the topology and geometry of root system architecture. It can also stored additional data such as the root type (from Plant Ontology), the root diameter and annotations.

 e
  
  {% for page in site.pages %}
  
  {% if page.tags contains 'example' %}
  
  <div class="example_block" markdown="1">
  
  <img src="image/example/{{ page.title }}_tn.png">
  
  <h5 markdown="1"> [{{ page.title }}]({{ page.url }}) </h5>
  
  {{ page.content }}  
  
  </div>
  
  {% endif %}
  
  {% endfor %}

[Back to RSML home](index)