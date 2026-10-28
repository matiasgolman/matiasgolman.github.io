---
layout: page
title: "CV"
permalink: /es/cv/
lang: "es"
alt_url: "/cv/"
standfirst: >-
  Microeconometrista y economista laboral aplicado, con experiencia de investigación en la OIT, la
  OCDE y el Banco Mundial. Ciudadanía argentina y polaca, radicado en Utrecht.
body_class: "listing"
description: >-
  Curriculum vitae de Matías Golman: profesor de Economía Aplicada en la Universidad de Utrecht,
  consultor de la OIT, antes OCDE y Banco Mundial. Doctor en Economía por la Universidad de
  Nottingham.
---

<p><a class="btn" href="{{ '/assets/pdf/cv-matias-golman.pdf' | relative_url }}">Descargar el PDF</a></p>

<div class="cv__section">
  <h2>Trayectoria</h2>
  {%- for r in site.data.cv_es.positions %}
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
  <h2>Formación</h2>
  {%- for r in site.data.cv_es.education %}
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
  <h2>Publicaciones seleccionadas</h2>
  {%- for p in site.data.papers_es.published %}
  <div class="cv__row">
    <div class="cv__when">{{ p.year }}</div>
    <div class="cv__what">
      <strong>{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</strong><br>
      <span class="cv__where">{{ p.where }}{% if p.authors %}, {{ p.authors }}{% endif %}</span>
    </div>
  </div>
  {%- endfor %}
  <p style="margin-top:1.4rem"><a href="{{ '/es/investigacion/' | relative_url }}">Documentos de trabajo e informes de política pública</a></p>
</div>

<div class="cv__section">
  <h2>Herramientas</h2>
  {%- for r in site.data.cv_es.skills %}
  <div class="cv__row">
    <div class="cv__when">{{ r.what }}</div>
    <div class="cv__what"><p style="margin-top:.25rem">{{ r.note }}</p></div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Idiomas</h2>
  {%- for r in site.data.cv_es.languages %}
  <div class="cv__row">
    <div class="cv__when">{{ r.what }}</div>
    <div class="cv__what"><p style="margin-top:.25rem">{{ r.note }}</p></div>
  </div>
  {%- endfor %}
</div>

<div class="cv__section">
  <h2>Comunidad</h2>
  <div class="cv__row">
    <div class="cv__when">2021–25</div>
    <div class="cv__what">
      <p style="margin-top:.25rem">Docente voluntario de inglés en Refugee Roots, Nottingham, con
      adultos solicitantes de asilo. Representante de posgrado y responsable de Igualdad,
      Diversidad e Inclusión en la Universidad de Nottingham.</p>
    </div>
  </div>
  <div class="cv__row">
    <div class="cv__when">2016–17</div>
    <div class="cv__what">
      <p style="margin-top:.25rem">Voluntario en la <a href="https://quieroayudar.org/organizaciones/asociacion-civil-avanzar-por-el-desarrollo-humano">Asociación Civil
      Avanzar por el Desarrollo Humano</a>, Buenos Aires, una organización de microcrédito. Mejoré
      sus bases de clientes para ajustar mejor los programas de préstamo, y di talleres de buenas
      prácticas de emprendimiento a los prestatarios.</p>
    </div>
  </div>
  <div class="cv__row">
    <div class="cv__when">2015–16</div>
    <div class="cv__what">
      <p style="margin-top:.25rem">Co-coordinador de un proyecto financiado por la UE de formación
      en emprendimiento sostenible para jóvenes en situación de desventaja en Tanzania, Nepal,
      Argentina, Portugal, Eslovenia e Italia.</p>
    </div>
  </div>
</div>
