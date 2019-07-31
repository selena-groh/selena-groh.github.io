---
layout: default
title: Projects
permalink: /projects/
---

{% for project in site.projects %}
  <!-- <h2>{% if project.link %}<a href="{{ project.link }}">{{ project.name }}</a>{% elsif project.github %}<a href="{{ project.github }}">{{ project.name }}</a>{% else %}{{ project.name }}{% endif %}</h2> -->
  <h2><a href="{{ project.url }}">{{ project.name }}</a></h2>
  <span>{{ project.time }}</span>
  {% if project.link %}<a href="{{ project.link }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/icon/link.svg#link' | relative_url }}"></use></svg></a>{% endif %}{% if project.github %}<a href="{{ project.github }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg></a>{% endif %}
  {% if project.img %}<img src="{{ project.img }}"/>{% endif %}
  <p>{{ project.content | markdownify }}</p>
{% endfor %}
