---
layout: page
title: Projects
permalink: /projects/
---

<div>
{% assign sorted = (site.projects | sort: 'order') %}
{% for project in sorted %}
  <!-- <h2>{% if project.link %}<a href="{{ project.link }}">{{ project.name }}</a>{% elsif project.github %}<a href="{{ project.github }}">{{ project.name }}</a>{% else %}{{ project.name }}{% endif %}</h2> -->
  <div class="row">
    <div class="card card-border">
      <div class="col-7">
        <!-- <h2><a href="{{ project.url }}">{{ project.name }}</a></h2> -->
        <h2>{{ project.name }}</h2>
        <span>{{ project.time }}&nbsp;</span>
        {% if project.link %}<a href="{{ project.link }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/icon/link.svg#link' | relative_url }}"></use></svg></a>{% endif %}{% if project.github %}<a href="{{ project.github }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg></a>{% endif %}
        <p>{{ project.content | markdownify }}</p>
        <ul class="tags">
          {% for tech in project.technologies %}
          <li>{{tech}}</li>
          {% endfor %}
        </ul>
      </div>
      <div class="col-5 right">
        {% if project.img %}<img src="{{ project.img }}"/>{% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>
