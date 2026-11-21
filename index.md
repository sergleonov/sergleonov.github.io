---
title: About
---

I'm a senior at Amherst College studying mathematics and computer science. My honors thesis is on numerical modeling of broadband cryogenic spectroscopy and collective dynamics in disordered quantum materials.

I work with Prof. Mattias Fitzpatrick at FitzLab, Dartmouth, simulating two-level-system defects coupled to bosonic environments and deriving time-optimal control for GKP states. I spent 2025–26 at Dartmouth as a visiting engineering student, where I also designed and simulated silicon photonic circuits with Prof. Anthony Rizzo.

Earlier projects took me through SAT solving, kinetic traffic models with optimal control, Markov chain sampling of binary matrices, and voice control for a Boston Dynamics Spot robot.

## News

<ul class="news">
{% for item in site.data.news limit:6 %}<li><time>{{ item.date | date: "%b %Y" }}</time><span>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}</span></li>
{% endfor %}
</ul>

## Selected publications

<ul class="pubs">
{% assign selected = site.data.publications | where: "selected", true %}
{% for pub in selected %}{% include pub.html pub=pub %}{% endfor %}
</ul>

[All publications]({{ '/publications/' | relative_url }})
