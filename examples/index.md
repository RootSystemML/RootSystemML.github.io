---
title: RSML Examples
layout: default
---

This page provides a set of example rsml files as well as the images the root architecture has been constructed from.
                                   
RSML allows to store a variety of content. The basic data contained in an RSML file is the topology and geometry of the root system architecture. It can also stored additional data such as the root type (from Plant Ontology), the root diameter and annotations.

[//]: # (list pages with tags example using liquid markup)
[//]: # (each page should have a xxx_tn.png image file in)
[//]: # (images/examples folder, with xxx the page title)


  {{ pages }}
  
  {% for page in site.pages reversed %}
  
  {% if page.tags contains 'example' %}
  
  <div class="example_block" markdown="1">
  
  <img src="/images/examples/{{ page.title }}_tn.png">
  
  <h5 markdown="1"> [{{ page.title }}]({{ page.url }}) </h5>
  
  {{ page.content }}
  
  </div>
  
  {% endif %}
  
  {% endfor %}

[Back to RSML home](index)