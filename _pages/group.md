---
layout: page
permalink: /group/
title: Research Group and Mentoring
description:  
years: [Postdoc, UIC, Other]
nav: false
heading: Research Group
---

<div class="publications">

Collaboration and mentoring are central to my research. I work with students and researchers across institutions and career stages, from high school research programs to graduate study and postdoctoral research. Our projects span geometry and mathematical physics, network dynamics, optimization, and mathematical modeling in the natural and social sciences.

Below you can meet my current and former students and postdoctoral researchers. You can also explore my <a href="/collaborators/">collaborators</a> and <a href="/visitors/">research visitors</a>.
 
 <br>
 <hr>
<span style="font-size:15px">

<h2>Current</h2>
 
 {%- for y in page.years %}
  {% bibliography -f current -q @*[year={{y}}]* %}
{% endfor %}

  <br>

 <hr>
<span style="font-size:15px">

<h2>Former</h2>


<div class="publications">

{%- for y in page.years %}
  {% bibliography -f past -q @*[year={{y}}]* %}
{% endfor %}

 
