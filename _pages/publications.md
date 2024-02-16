---
layout: page
permalink: /publications/
title: Papers
description: 
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

* denotes equal contribution

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}


</div>
