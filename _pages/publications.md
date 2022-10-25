---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2022]
nav: true
nav_order: 1
---
You can also find my publications on my [Google Scholar](https://scholar.google.com/citations?hl=en&user=twh30v0AAAAJ) 
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
