---
layout: page
permalink: /publications/
title: Papers
years: []
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

  <!-- Undated first -->
  {% bibliography -f {{ site.scholar.bibliography }} -q @* --template bib_noyear %}

  <!-- Then the explicit years -->
  {%- for y in page.years %}
    <h2 class="year">{{ y }}</h2>
    {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{ y }}]* %}
  {%- endfor %}

</div>
