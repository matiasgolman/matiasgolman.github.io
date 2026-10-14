---
layout: page
title: "Investigación y política pública"
permalink: /es/investigacion/
lang: "es"
alt_url: "/work/"
standfirst: >-
  Documentos de trabajo, artículos publicados y los informes que escribí para organismos
  internacionales. Casi todo es sobre empleo informal, habilidades y cómo tratan los mercados de
  trabajo a quienes tienen menos margen para absorber un golpe.
body_class: "listing"
description: >-
  Documentos de trabajo, artículos y informes de política pública de Matías Golman sobre empleo
  informal, demanda de habilidades, formalización y protección social, para la OIT, la OCDE y el
  Banco Mundial.
---

<h2>Documentos de trabajo</h2>
<ul class="entries">
  {%- for p in site.data.papers_es.working %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{{ p.title }}</h3>
      <p class="entry__meta">{{ p.sub }}{% if p.authors %}. {{ p.authors }}{% endif %}{% if p.where %}. {{ p.where }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
      {%- if p.abstract %}<details class="abstract"><summary>Resumen</summary><p>{{ p.abstract }}</p></details>{% endif %}
      {%- if p.pdf %}<p class="entry__links"><a href="{{ p.pdf | relative_url }}">PDF</a></p>{% endif %}
    </div>
  </li>
  {%- endfor %}
  {%- for p in site.data.papers_es.inprogress %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{{ p.title }}</h3>
      <p class="entry__meta">En curso{% if p.authors %}. {{ p.authors }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>

<h2>Artículos publicados</h2>
<ul class="entries">
  {%- for p in site.data.papers_es.published %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</h3>
      <p class="entry__meta">{{ p.where }}{% if p.authors %}, {{ p.authors }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
      {%- if p.pdf %}<p class="entry__links"><a href="{{ p.pdf | relative_url }}">PDF</a></p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>

<h2>Trabajo de política pública</h2>
<ul class="entries">
  {%- for p in site.data.papers_es.policy %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</h3>
      <p class="entry__meta">{{ p.org }}{% if p.authors %}, {{ p.authors }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
      {%- if p.pdf %}<p class="entry__links"><a href="{{ p.pdf | relative_url }}">PDF</a></p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>
