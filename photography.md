---
layout: page
title: "Photography"
permalink: /photography/
body_class: "listing"
page_class: "page--wide"
standfirst: >-
  Mountains, forests, water and the odd bird, from Patagonia, the Alps, Scotland, Greece, Norway
  and the flat country I live in now. I refill my energy and spirit when I am in nature, and the
  camera tends to come out while I am at it.
description: >-
  Landscape and nature photographs by Matías Golman, from Patagonia, the Alps, Scotland, Greece,
  Norway and the Netherlands.
---

<div class="gallery" role="img" aria-label="A gallery of {{ site.data.photos | size }} landscape and nature photographs: mountains, lakes, glaciers, forests, coastlines, flowers and birds.">
  {%- for p in site.data.photos %}
  <img class="shot" src="{{ '/assets/img/photos/' | append: p.slug | append: '.jpg' | relative_url }}"
       alt="" width="{{ p.w }}" height="{{ p.h }}" loading="lazy" decoding="async">
  {%- endfor %}
</div>

<p class="gallery__note">{{ site.data.photos | size }} photographs, taken on whatever I had in my
pocket at the time. More of them on <a href="https://www.instagram.com/gol.mat/">Instagram</a>.</p>
