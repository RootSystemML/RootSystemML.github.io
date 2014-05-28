---
title: RSML Examples
layout: default
---

This page provides a set of example rsml files as well as the images the root systems have been constructed from.

RSML allows to store a variety of content. The basic data contained in an RSML file are the topology and geometry of the root system architecture. Then it can stored additional data such as the root type (from Plant Ontology), the root diameter and annotations.

[//]: # (list pages with tags example using liquid markup)
[//]: # (each page should have a xxx_tn.png image file in)
[//]: # (images/examples folder, with xxx the page title)

a

  {{ pages }}
  
  {% for page in site.pages sort_by:title order:ascending %}
  
  {% if page.tags contains 'example' %}
  
  <div class="example_block" markdown="1">
  
  <img src="/images/examples/{{ page.title }}_tn.png">
  
  <h5 id="{{ page.title }}" markdown="1"> [{{ page.title }}]({{ page.url }}) </h5>
  
  {{ page.content }}
  
  </div>
  
  {% endif %}
  
  {% endfor %}

[Back to RSML home](index)