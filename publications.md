---
title: Publications
---

Also on [Google Scholar](https://scholar.google.com/citations?user={{ site.author.scholar }}).

{% assign years = site.data.publications | map: "year" | compact | uniq | sort | reverse %}
{% for y in years %}
<h3 class="year">{{ y }}</h3>
<ul class="pubs">
{% assign pubs_in_year = site.data.publications | where: "year", y %}
{% for pub in pubs_in_year %}{% include pub.html pub=pub %}{% endfor %}
</ul>
{% endfor %}

{% assign upcoming = site.data.publications | where: "status", "in preparation" %}
{% if upcoming.size > 0 %}
<h3 class="year">In preparation</h3>
<ul class="pubs">
{% for pub in upcoming %}{% include pub.html pub=pub %}{% endfor %}
</ul>
{% endif %}

## Presentations

<ul class="pubs">
<li class="pub"><span class="pub-title">Defects in Sync: Modeling Material Flaws That Disrupt Quantum Computers</span><span class="pub-authors"><strong>S. Leonov</strong>, S. Bedkihal, and S. Alfeld</span><span class="pub-venue">Summer Undergraduate Research Poster Session, Amherst College, 2026</span></li>
<li class="pub"><span class="pub-title">“Hey Daisy”: A Real-Time Voice Control Interface for Spot Robot</span><span class="pub-authors"><strong>S. Leonov</strong> and S. Alfeld</span><span class="pub-venue">Summer Undergraduate Research Poster Session, Amherst College, 2025</span></li>
<li class="pub"><span class="pub-title">StolenBase: Faster Sampling of Fixed-Margin Binary Matrices</span><span class="pub-authors">M. Riondato, <strong>S. Leonov</strong>, and M. Li</span><span class="pub-venue">Summer Undergraduate Research Poster Session, Amherst College, 2024</span></li>
</ul>
