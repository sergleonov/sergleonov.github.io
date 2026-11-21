---
title: Projects
---

More on [GitHub](https://github.com/{{ site.author.github }}).

<ul class="projects">
{% for p in site.data.projects %}{% include project.html project=p %}
{% endfor %}
</ul>
