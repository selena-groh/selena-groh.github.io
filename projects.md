---
layout: page
title: Projects
permalink: /projects/
---

<div>
{% assign sorted = (site.projects | sort: 'order') %}
{% for project in sorted %}
  {% if project.link %}
    {% assign primaryLink = project.link %}
  {% else %}
    {% assign primaryLink = project.github %}
  {% endif %}
  <div class="row">
      <div class="card card-border card-background card-fullWidth">
        <div class="col-7">
          {% if primaryLink %}
            <h2><a href="{{ primaryLink }}">{{ project.name }}</a></h2>
          {% else %}
            <h2>{{ project.name }}</h2>
          {% endif %}
          <span>{{ project.time }}&nbsp;</span>
          {% if project.link %}<a target="_blank" href="{{ project.link }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/icon/link.svg#link' | relative_url }}"></use></svg></a>{% endif %}{% if project.github %}<a target="_blank" href="{{ project.github }}"><svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg></a>{% endif %}
          <p>{{ project.content | markdownify }}</p>
          <ul class="tags">
            {% for tech in project.technologies %}
            <li>{{tech}}</li>
            {% endfor %}
          </ul>
        </div>
        <div class="col-5 center">
          {% if project.img %}
            {% if primaryLink %}
              <a href="{{ primaryLink }}" target="_blank">
                <img src="{{ project.img }}"/>
              </a>
            {% else %}
              <img src="{{ project.img }}"/>
            {% endif %}
          {% endif %}
        </div>
      </div>
  </div>
{% endfor %}
</div>
