---
layout: page
title: Design
permalink: /design/
images:
  - image_path: /assets/img/design/MelancholyPlay.png
    title: Melancholy Play
    orientation: vertical
  - image_path: /assets/img/design/Red.png
    title: Red
    orientation: vertical
  - image_path: /assets/img/design/ILY.png
    title: I Love You, You're Perfect, Now Change
    orientation: vertical
  - image_path: /assets/img/design/24-Hour.png
    title: 24-Hour Play Festival
    orientation: horizontal
  - image_path: /assets/img/design/UmbrellaGroupShowcase.png
    title: Umbrella Group Showcase
    orientation: horizontal
  - image_path: /assets/img/design/Dutchman.png
    title: Dutchman
    orientation: horizontal
---

I've designed a number of posters and graphics, primarily for Tufts University's [Pen, Paint, and Pretzels](http://tufts3ps.com/) student theater and performance organization.

My primary tools are [Adobe Photoshop](https://www.adobe.com/products/photoshopfamily.html), [GIMP](https://www.gimp.org/), [Google Fonts](https://fonts.google.com/), and [Canva](https://www.canva.com/).

<ul class="photo-gallery">
  {% for image in page.images %}
    <li class="card {{ image.orientation }}"><img src="{{ image.image_path }}" alt="{{ image.title}}"/>
      <!-- <p class="text">{{ image.title}}</p> -->
    </li>
  {% endfor %}
</ul>
