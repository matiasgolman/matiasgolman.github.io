---
layout: page
title: "Some pictures"
permalink: /pictures/
body_class: "listing"
page_class: "page--wide"
standfirst: >-
  I take these with my phone whenever I am somewhere with nice nature. No editing involved.
description: >-
  Nature pictures taken by Matías Golman in Patagonia, the Alps, Scotland, Greece, Norway and the
  Netherlands.
lang: "en"
alt_url: "/es/fotos/"
---

<div class="gallery" role="img" aria-label="A gallery of {{ site.data.photos | size }} nature pictures: mountains, lakes, glaciers, forests, coastlines, flowers and birds.">
  {%- for p in site.data.photos %}
  <img class="shot" src="{{ '/assets/img/photos/' | append: p.slug | append: '.jpg' | relative_url }}"
       alt="" width="{{ p.w }}" height="{{ p.h }}" loading="lazy" decoding="async">
  {%- endfor %}
</div>

<p class="gallery__note">{{ site.data.photos | size }} pictures. More on
<a href="https://www.instagram.com/gol.mat/">Instagram</a>.</p>
