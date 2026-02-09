---
layout: page
permalink: /preprints/
title: Preprints
description: All the preprints that I have done or collaborated with. (†:Equal contribution)
sections:
   - bibquery: "@preprints"
     text: "Preprints"
   

nav: true
---

<!-- _pages/random.md -->
 
 <div class="publications">
 
 {% for section in page.sections %}
 
   <a id="{{section.text}}"></a>
   <!-- <p class="bibtitle">{{section.text}}</p> -->
 
   {%- bibliography -f papers -q {{section.bibquery}} -%}
 
 {% endfor %}