---
title: Projects
---

More on [GitHub](https://github.com/{{ site.author.github }}).

<ul class="pubs">
{% for p in site.data.projects %}<li class="pub"><span class="pub-title">{{ p.title }}</span>{% if p.team %}<span class="pub-venue">{{ p.team }}</span>{% endif %}<span class="pub-authors">{{ p.text }}</span>{% if p.github != "" %}<span class="pub-links"><a href="{{ p.github }}">GitHub</a></span>{% endif %}</li>
{% endfor %}
</ul>
