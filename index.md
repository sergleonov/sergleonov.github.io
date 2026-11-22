---
title: About
---

I'm a senior at Amherst College studying mathematics and computer science. My third-year I spent at Dartmouth College as a Dual Degree Engineering student, where I joined Mattias Fitzpatrick's FitzLab. I am writing my honors thesis on numerical modeling of broadband cryogenic spectroscopy and collective dynamics in disordered quantum materials under Prof. Scott Alfeld (Amherst) and Dr. Salil Bedkihal (Dartmouth).

My earlier research involved simulating integrated photonic devices in Lumerical (FDTD/Mode/Interconnect), creating a voice control interface for a Boston Dynamics Spot robot, implementing a new SAT-solving procedure, modeling autonomous traffic with optimal control, and developing a randomized algorithm for Bayesian sampling of binary matrices.

Outside academics, I've played ice hockey most of my life. I have played in Spartak and CSKA academies back in Russia, making it up to Divsion III at Amherst. These days I play occasional pick up soccer and enjoy watching Messi highlights with a cup of good coffee.

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
