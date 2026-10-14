---
layout: page
title: "Projects"
permalink: /projects/
standfirst: >-
  Two things I built because the analysis wasn't much use until someone else could open it.
body_class: ""
description: >-
  The Argentina Informality Dashboard, built for the ILO from two decades of household survey
  microdata, and Araucaria Spotter, a community map of monkey puzzle trees outside their native range.
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
  <p>The dashboard is a large page — it carries the full series rather than calling a server for
  them — so give it a moment to load on a slow connection.</p>
</div>
