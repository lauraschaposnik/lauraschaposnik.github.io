---
layout: page
order: 2
permalink: /media/
title: Media
description: 
years: [2026, 2025, 2024, 2023, 2022, 2021,2020,2019,2018,2017,2016,2009]
nav: false
heading: Media
---
 
 My work within geometry as well as on interdisciplinary areas and outreach has been featured in <b> 40+ </b> media outlets.
 
 <div class="press-kit callout" style="border:1px solid #eee;border-radius:12px;padding:14px 16px;margin:18px 0;background:#fafafa">
  <strong>Press kit</strong> — quick headshots, short/long bios, and copy‑ready facts for journalists & organizers.
  <br>
  <a href="{{ '/media/press-kit/' | relative_url }}" class="btn">Open press kit →</a>
  <span style="margin-left:10px">
    • <a href="{{ '/assets/img/prof_pic.jpg' | relative_url }}">Headshot (JPG)</a>
    • <a href="{{ '/assets/cv/laura_schaposnik_cv.pdf' | relative_url }}"> CV</a>
  </span>
</div>

 
 Here you can find a quasi-complete list, with information on the topic appearing in the <b>Abs</b> buttons, and links to the media within the title. 

<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  {% bibliography -f media -q @*[year={{y}}]* %}
{% endfor %}

</div>
