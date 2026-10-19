---
layout: page
title: "Lo que construí"
permalink: /es/proyectos/
lang: "es"
alt_url: "/projects/"
standfirst: >-
  Dos cosas que hice y puse online. Una salió de una consultoría, la otra de la costumbre de mirar
  los árboles.
body_class: "listing"
page_class: "page--wide"
description: >-
  El Panel de informalidad en América Latina, hecho con microdatos de encuestas de
  hogares de Argentina y Costa Rica, y Araucaria Spotter, un mapa comunitario de pehuenes fuera de su rango
  nativo.
---

<div class="tools">
  {%- for t in site.data.projects_es %}
  <article class="tool">
    <img class="tool__shot" src="{{ t.shot | relative_url }}" alt="{{ t.shot_alt }}" loading="lazy" width="432" height="324">
    <div>
      <h2 class="tool__name" style="margin-top:0"><a href="{% if t.external %}{{ t.url }}{% else %}{{ t.url | relative_url }}{% endif %}">{{ t.name }}</a></h2>
      <p>{{ t.blurb }}</p>
      <p class="tool__note">{{ t.note }}</p>
    </div>
  </article>
  {%- endfor %}
</div>

<div class="prose" style="margin-top:3rem">
  <p>El panel es una página pesada, porque lleva adentro la serie completa en vez de pedírsela a un
  servidor. Dale un momento para cargar si tenés poca conexión.</p>
</div>
