---
layout: page
permalink: /publications/
title: Publications
description: All the publications that I have done or collaborated with. (†:Equal contribution)
sections:
  - bibquery: "@preprints @inproceedings @article"
    text: "All Publications"
    years: [2025, 2024, 2023, 2022]

nav: true
---
<!-- _pages/publications.md -->

<div class="publications">

{% for section in page.sections %}
  <a id="{{section.text}}"></a>
  <p class="bibtitle">{{section.text}}</p>

  {%- for y in section.years %}
    <!-- <h2 class="year">{{y}}</h2> -->
    {%- bibliography -f papers -q {{section.bibquery}}[year={{y}}] -%}
  {% endfor %}
  
{% endfor %}

</div>