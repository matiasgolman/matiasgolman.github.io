---
layout: page
title: "CV"
permalink: /cv/
standfirst: >-
  Micro-econometrician and applied labour economist, with research experience at the ILO, the OECD
  and the World Bank. Argentinian and Polish citizenship, based in Utrecht.
body_class: "listing"
description: >-
  Curriculum vitae of Matías Golman: Lecturer in Applied Economics at Utrecht University, consultant
  for the ILO, previously OECD and World Bank. PhD in Economics, University of Nottingham.
lang: "en"
alt_url: "/es/cv/"
---

<p><a class="btn" href="{{ '/assets/pdf/cv-matias-golman.pdf' | relative_url }}">Download the PDF</a></p>

<div class="cv__section">
  <h2>Positions</h2>
  {%- for r in site.data.cv.positions %}
  <div class="cv__row">
    <div class="cv__when">{{ r.when }}</div>
    <div class="cv__what">
      <strong>{{ r.what }}</strong><br>
      <span class="cv__where">{{ r.where }}</span>
      <p>{{ r.note }}</p>
    </div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Education</h2>
  {%- for r in site.data.cv.education %}
  <div class="cv__row">
    <div class="cv__when">{{ r.when }}</div>
    <div class="cv__what">
      <strong>{{ r.what }}</strong><br>
      <span class="cv__where">{{ r.where }}</span>
      <p>{{ r.note }}</p>
    </div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Selected publications</h2>
  {%- for p in site.data.papers.published %}
  <div class="cv__row">
    <div class="cv__when">{{ p.year }}</div>
    <div class="cv__what">
      <strong>{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</strong><br>
      <span class="cv__where">{{ p.where }}{% if p.authors %}, {{ p.authors }}{% endif %}</span>
    </div>
  </div>
  {%- endfor %}
  <p style="margin-top:1.4rem"><a href="{{ '/work/' | relative_url }}">Working papers and policy reports</a></p>
</div>

<div class="cv__section">
  <h2>Skills</h2>
  {%- for r in site.data.cv.skills %}
  <div class="cv__row">
    <div class="cv__when">{{ r.what }}</div>
    <div class="cv__what"><p style="margin-top:.25rem">{{ r.note }}</p></div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Languages</h2>
  {%- for r in site.data.cv.languages %}
  <div class="cv__row">
    <div class="cv__when">{{ r.what }}</div>
    <div class="cv__what"><p style="margin-top:.25rem">{{ r.note }}</p></div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Community</h2>
  <div class="cv__row">
    <div class="cv__when">2021–25</div>
    <div class="cv__what">
      <p style="margin-top:.25rem">Volunteer English teacher at Refugee Roots, Nottingham, with adults
      seeking asylum. Postgraduate representative and Equality, Diversity and Inclusion officer at the
      University of Nottingham.</p>
    </div>
  </div>
  <div class="cv__row">
    <div class="cv__when">2015–16</div>
    <div class="cv__what">
      <p style="margin-top:.25rem">Co-coordinator of an EU-funded training project on sustainable
      entrepreneurship for disadvantaged youth across Tanzania, Nepal, Argentina, Portugal, Slovenia
      and Italy.</p>
    </div>
  </div>
</div>
