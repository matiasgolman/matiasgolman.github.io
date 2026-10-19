---
layout: page
title: "Things I've built"
permalink: /projects/
standfirst: >-
  Two things I made and put online. One came out of a consultancy, the other out of a habit of
  looking up at trees.
body_class: "listing"
page_class: "page--wide"
description: >-
  The Latin America Informality Dashboard, built from household survey microdata of
  Argentina and Costa Rica, and Araucaria Spotter, a community map of monkey puzzle trees growing outside their
  native range.
lang: "en"
alt_url: "/es/proyectos/"
---

<div class="tools">
  {%- for t in site.data.projects %}
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
  <p>The dashboard is a large page, because it carries the full series rather than calling a
  server for them. Give it a moment to load on a slow connection.</p>
</div>
