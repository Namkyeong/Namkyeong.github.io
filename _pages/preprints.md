---
layout: page
permalink: /preprints/
title: Preprints
description: All the preprints that I have done or collaborated with. (†:Equal contribution)
sections:
   - bibquery: "@preprints"
     text: "Preprints"
     years: [2025]
   

nav: true
---

<!-- _pages/random.md -->
 
 <div class="publications">
 
 {% for section in page.sections %}
 
   <a id="{{section.text}}"></a>
   <!-- <p class="bibtitle">{{section.text}}</p> -->
 
   {%- for y in section.years %}
    <h2 class="year">{{y}}</h2>
     {%- bibliography -f papers -q {{section.bibquery}}[year={{y}}] -%}
   {% endfor %}
 
 {% endfor %}