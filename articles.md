---
layout: page
title: "News articles"
permalink: /articles/
standfirst: >-
  Columns I write for newspapers, mostly in Argentina and in Spanish, each with a technical report in English that
  sets out the data, the methods and the assumptions behind every number.
body_class: "listing"
description: >-
  News articles by Matías Golman: newspaper columns on labour markets, households and public policy, each with an
  English technical report on data, methods and assumptions.
lang: "en"
alt_url: "/es/notas/"
---

{%- assign notas = site.pages | where: "layout", "nota" | where: "lang", "en" | sort: "date" | reverse %}
{% include notas-list.html items=notas %}
