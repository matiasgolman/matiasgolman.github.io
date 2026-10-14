---
layout: page
title: "Fotografía"
permalink: /es/fotografia/
lang: "es"
alt_url: "/photography/"
standfirst: >-
  Me encanta estar en la naturaleza, y saco fotos cuando viajo. Estas son algunas.
body_class: "listing"
page_class: "page--wide"
description: >-
  Fotografías de paisaje y naturaleza de Matías Golman, de la Patagonia, los Alpes, Escocia,
  Grecia, Noruega y los Países Bajos.
---

<div class="gallery" role="img" aria-label="Una galería de {{ site.data.photos | size }} fotografías de paisaje y naturaleza: montañas, lagos, glaciares, bosques, costas, flores y aves.">
  {%- for p in site.data.photos %}
  <img class="shot" src="{{ '/assets/img/photos/' | append: p.slug | append: '.jpg' | relative_url }}"
       alt="" width="{{ p.w }}" height="{{ p.h }}" loading="lazy" decoding="async">
  {%- endfor %}
</div>

<p class="gallery__note">{{ site.data.photos | size }} fotografías. Hay más en
<a href="https://www.instagram.com/gol.mat/">Instagram</a>.</p>
