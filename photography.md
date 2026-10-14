---
layout: page
title: "Photography"
permalink: /photography/
body_class: "listing"
page_class: "page--wide"
standfirst: >-
  I love being in nature, and I take photographs when I travel. These are some of them.
description: >-
  Landscape and nature photographs by Matías Golman, from Patagonia, the Alps, Scotland, Greece,
  Norway and the Netherlands.
lang: "en"
alt_url: "/es/fotografia/"
---

<div class="gallery" role="img" aria-label="A gallery of {{ site.data.photos | size }} landscape and nature photographs: mountains, lakes, glaciers, forests, coastlines, flowers and birds.">
  {%- for p in site.data.photos %}
  <img class="shot" src="{{ '/assets/img/photos/' | append: p.slug | append: '.jpg' | relative_url }}"
       alt="" width="{{ p.w }}" height="{{ p.h }}" loading="lazy" decoding="async">
  {%- endfor %}
</div>

<p class="gallery__note">{{ site.data.photos | size }} photographs. More on
<a href="https://www.instagram.com/gol.mat/">Instagram</a>.</p>
