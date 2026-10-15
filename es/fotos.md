---
layout: page
title: "Algunas fotos"
permalink: /es/fotos/
lang: "es"
alt_url: "/pictures/"
standfirst: >-
  Las saco con el teléfono cada vez que estoy en algún lugar con naturaleza linda. Sin edición de
  por medio.
body_class: "listing"
page_class: "page--wide"
description: >-
  Fotos de naturaleza sacadas por Matías Golman en la Patagonia, los Alpes, Escocia, Grecia,
  Noruega y los Países Bajos.
---

<div class="gallery" role="img" aria-label="Una galería de {{ site.data.photos | size }} fotos de naturaleza: montañas, lagos, glaciares, bosques, costas, flores y aves.">
  {%- for p in site.data.photos %}
  <img class="shot" src="{{ '/assets/img/photos/' | append: p.slug | append: '.jpg' | relative_url }}"
       alt="" width="{{ p.w }}" height="{{ p.h }}" loading="lazy" decoding="async">
  {%- endfor %}
</div>

<script>
  // Baraja la galería en cada visita, así no se ve siempre el mismo arriba.
  // Corre antes de pintar, de modo que loading="lazy" pide sólo las que quedan a la vista.
  (function () {
    var g = document.querySelector('.gallery');
    if (!g) return;
    var shots = Array.prototype.slice.call(g.children);
    for (var i = shots.length - 1; i > 0; i--) {
      var j = Math.floor(Math.random() * (i + 1));
      g.appendChild(shots[j]);
      shots.splice(j, 1);
    }
  })();
</script>

<p class="gallery__note">{{ site.data.photos | size }} fotos. Hay más en
<a href="https://www.instagram.com/gol.mat/">Instagram</a>.</p>
