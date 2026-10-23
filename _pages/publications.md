---
layout: page
order: 2
permalink: /publications/
title: Publications
description: 
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
nav: false
heading: Publications
---

<!-- _pages/publications.md -->

<script>
function filterSubject(filter) {
  var list = document.getElementById("publicationList");
  var rows = list.getElementsByClassName("row");
  
  // Loop through all rows, hide those which don't match the selected filter
  for (i = 0; i < rows.length; i++) {
    var primaryClass = rows[i].getElementsByClassName("category-tag")[0];
	if (primaryClass.textContent.indexOf(filter) > -1) {
        rows[i].style.display = "";
    } else {
        rows[i].style.display = "none";
    }
  }
  
  // Loop through all sections, hide those which are empty
  var years = list.getElementsByClassName("year");
  for (i = 0; i < years.length; i++) {
    var count = 0;
    for (j = 0; j < rows.length; j++) {
	  var section_tag = rows[j].getElementsByClassName("section-tag")[0];
	  if (section_tag.textContent == years[i].textContent && rows[j].style.display == "") { count++; }
	}
	if (count != 0) {
	  years[i].style.display = "";
	} else {
	  years[i].style.display = "none";
	}
  }
}
</script>


My research spans pure and applied mathematics. In geometry and mathematical physics, I study Higgs bundles, Hitchin systems, and moduli spaces of decorated bundles, with particular interests in spectral data, branes, geometric structures, and their connections to representation theory and the Langlands program.

In applied mathematics, I develop and study mathematical models and algorithms for complex systems. My work includes network dynamics and contagion, synchronization and collective behavior, optimization and sensor placement, and data-informed forecasting. These projects combine mathematical analysis, computation, and collaboration across disciplines, with applications in the natural and social sciences.

Below you can explore my publications by research area. I have also included the children’s books I have published to teach mathematics or introduce mathematical ideas. For the complete collection, please visit my <a href="https://lauraschaposnik.com/books/">Children’s Books page</a>.

<center>
<p>
<abbr class="{{site.data.badge_colors['darkgrey']}}" onclick="filterSubject('')" style="cursor: pointer;">All</abbr>&ensp;
<abbr class="{{site.data.badge_colors['cyan']}}" onclick="filterSubject('geometry')" style="cursor: pointer;">Geometry</abbr>&ensp;
<abbr class="{{site.data.badge_colors['blue']}}" onclick="filterSubject('applied')" style="cursor: pointer;">Interdisciplinary</abbr>&ensp;
<abbr class="{{site.data.badge_colors['green']}}" onclick="filterSubject('books')" style="cursor: pointer;">Children Books</abbr>&ensp;
</p>
</center>

My <b>45+ pieces</b> both within geometry as well as on other topics are listed below in reverse chronological order by year. Note that authors on all of my publications appear alphabetically except in our Nature Scientific Reports paper, where authors are by contribution. Here is a very useful MIT whiteboard software to collaborate with people: <a href="https://cocreate.csail.mit.edu/">Co-create</a>. 
Citations to my papers can be found on <a href="https://scholar.google.com/citations?user=5cLd6dIAAAAJ&hl=en">Google Scholar</a>.
Paper tags are colored as follows:

<center>
<p>
<span class="badge badge-danger">journal article</span>
<span class="badge badge-primary">conference article</span> 
<span class="badge badge-warning">editorial work</span> 
<span class="badge badge-light">manuscript</span> .
</p>
</center>

<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
