---
layout: page
title: Design
permalink: /design/
images:
  - image_path: /assets/img/design/MelancholyPlay.jpg
    title: Melancholy Play
    orientation: vertical
  - image_path: /assets/img/design/Red.jpg
    title: Red
    orientation: vertical
  - image_path: /assets/img/design/ILY.jpg
    title: I Love You, You're Perfect, Now Change
    orientation: vertical
  - image_path: /assets/img/design/24-Hour.jpg
    title: 24-Hour Play Festival
    orientation: horizontal
  - image_path: /assets/img/design/UmbrellaGroupShowcase.jpg
    title: Umbrella Group Showcase
    orientation: horizontal
  - image_path: /assets/img/design/Dutchman.jpg
    title: Dutchman
    orientation: horizontal
tools:
  - image_path: /assets/icon/photoshop.png
    title: Adobe Photoshop
    link: https://www.adobe.com/products/photoshopfamily.html
  - image_path: /assets/icon/gimp.png
    title: GIMP
    link: https://www.gimp.org/
  - image_path: /assets/icon/google_fonts.png
    title: Google Fonts
    link: https://fonts.google.com/
  - image_path: /assets/icon/coolors.png
    title: Coolors
    link: https://coolors.co/
  - image_path: /assets/icon/canva.png
    title: Canva
    link: https://www.canva.com/
---

I've designed a number of posters and graphics, primarily for Tufts University's [Pen, Paint, and Pretzels](http://tufts3ps.com/) student theater and performance organization.

## Tools

<div>
  <div class="row row-center">
    {% for tool in page.tools %}
      <a class="col-6-sm col-3-md col-2 center card card-box-shadow" href="{{ tool.link }}">
        <p><img src="{{ tool.image_path }}" alt="{{ tool.title}}"/></p>
        <span>{{ tool.title }}</span>
      </a>
    {% endfor %}
  </div>
</div>

## Work

<div>
  <div class="row">
    {% for image in page.images %}
      <div class="{% if image.orientation == 'vertical' %}col-4-md{% else %}col-12{% endif %}">
        <a target="_blank" href="{{ image.image_path }}"><img src="{{ image.image_path }}" alt="{{ image.title}}"/></a>
      </div>
    {% endfor %}
  </div>
</div>
