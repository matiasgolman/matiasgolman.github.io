---
layout: page
title: "Notas"
permalink: /es/notas/
lang: "es"
alt_url: "/commentary/"
standfirst: >-
  Notas que escribo para diarios, sobre todo en la Argentina, cada una con un reporte técnico que explica los datos,
  los métodos y los supuestos detrás de cada cifra.
body_class: "listing"
description: >-
  Notas de Matías Golman en diarios sobre mercado de trabajo, hogares y políticas públicas, cada una con su reporte
  técnico: datos, métodos y supuestos.
---

{%- assign notas = site.pages | where: "layout", "nota" | where: "lang", "es" | sort: "date" | reverse %}
{% include notas-list.html items=notas %}
