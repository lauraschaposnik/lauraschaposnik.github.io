---
layout: page
order: 2
permalink: /publications/
title: Publications
description: 
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
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





My research is both in geometry (moduli spaces, Higgs bundles and related fields) and more applied mathematics. I am interested in the study of the geometry and topology of the moduli spaces of Higgs bundles, integrable systems and decorated bundles, and the geometric structures they parametrize.   In particular, I am interested in understanding  of branes of Higgs bundles,  dualities within quiver varieties in general, and within generalized hyperpolygons in particular, with views towards applications to the Langlands program for wild Hitchin systems. In a different direction, I am interested in the appearances  of  geometric structures and symmetries within different areas of sciences, which has led to some publications in applied mathematics. You can see my work in each area by clicking on the links below (I have included here the children books I have published to teach mathematics or about mathematics -- for a complete list of my children books, please visit my  <a href="https://lauraschaposnik.com/books/">Children Books page</a>.

<center>
<p>
<abbr class="{{site.data.badge_colors['darkgrey']}}" onclick="filterSubject('')" style="cursor: pointer;">All</abbr>&ensp;
<abbr class="{{site.data.badge_colors['cyan']}}" onclick="filterSubject('geometry')" style="cursor: pointer;">Geometry</abbr>&ensp;
<abbr class="{{site.data.badge_colors['blue']}}" onclick="filterSubject('applied')" style="cursor: pointer;">Interdisciplinary</abbr>&ensp;
<abbr class="{{site.data.badge_colors['green']}}" onclick="filterSubject('books')" style="cursor: pointer;">Children Books</abbr>&ensp;
</p>
</center>

My <b>45+ pieces</b> both within geometry as well as on other topics are listed below in reverse chronological order by year. Note that authors on all of my publications appear alphabetically except in our Nature Scientific Reports paper, where authors are by contribution.
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
