---
layout: page
title: "Research and policy work"
permalink: /work/
standfirst: >-
  Working papers, published articles, and the reports I have written for international
  organisations. Most of it is about informal employment, skills, and how labour markets treat the
  people with the least room to absorb a shock.
body_class: "listing"
description: >-
  Working papers, peer-reviewed articles and policy reports by Matías Golman on informal employment,
  skills demand, formalisation policy and social protection, for the ILO, the OECD and the World Bank.
lang: "en"
alt_url: "/es/investigacion/"
---

<h2>Working papers</h2>
<ul class="entries">
  {%- for p in site.data.papers.working %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{{ p.title }}</h3>
      <p class="entry__meta">{{ p.sub }}{% if p.authors %}. {{ p.authors }}{% endif %}{% if p.where %}. {{ p.where }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
      {%- if p.abstract %}<details class="abstract"><summary>Abstract</summary><p>{{ p.abstract }}</p></details>{% endif %}
      {%- if p.pdf %}<p class="entry__links"><a href="{{ p.pdf | relative_url }}">PDF</a></p>{% endif %}
    </div>
  </li>
  {%- endfor %}
  {%- for p in site.data.papers.inprogress %}
  <li class="entry">
    <div class="entry__when">{{ p.year }}</div>
    <div>
      <h3 class="entry__title">{{ p.title }}</h3>
      <p class="entry__meta">Work in progress{% if p.authors %}. {{ p.authors }}{% endif %}</p>
      {%- if p.text %}<p class="entry__text">{{ p.text }}</p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>

<h2>Published articles</h2>
<ul class="entries">
  {%- for p in site.data.papers.published %}
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

<h2>Policy work</h2>
<ul class="entries">
  {%- for p in site.data.papers.policy %}
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
