---
layout: page
title: "Latin America Informality Dashboard"
permalink: /dashboard/
standfirst: >-
  Household survey microdata on informal employment in Latin America, in a form you can
  interrogate rather than read about, one country at a time or side by side.
body_class: "listing"
page_class: "page--wide page--dash"
description: >-
  Interactive dashboard of informal employment in Latin America, built from each country's official
  household survey, with rates by sector, region, urban and rural areas, sex and age, and a country
  comparison. An independent project by Matías Golman.
lang: "en"
alt_url: "/es/panel/"
---

<p>Informal employment is one of the most persistent problems of Latin American labour markets,
and most countries measure it every quarter. The trouble is that the measurement sits in raw survey
files that almost nobody outside a statistics office opens. This dashboard turns those files into
something a policy officer, a journalist or a union researcher can actually use: informality broken
down by sector, region, sex and age, one country at a time, or several side by side. It grows one
country at a time, each from the earliest year its survey allows.</p>

<p class="tool__note">Countries and sources so far: {% for c in site.data.informality_countries %}{{ c.name_en }}
(from {{ c.since }}; {{ c.source_en }}){% unless forloop.last %}; {% endunless %}{% endfor %}. An independent project, which grew out of consultancy work on
labour informality in Argentina. Each country's official measure reproduces the
informality rates its statistics office publishes. Definitions differ between countries, so the
comparison view works with trends and says what is not comparable.</p>

{% include dashboard-embed.html
   title="Latin America Informality Dashboard"
   fullscreen="Open the dashboard in its own tab" %}

<p style="margin-top:1.4rem"><a href="{{ '/projects/' | relative_url }}">Other things I've
built</a>, or <a href="{{ '/work/' | relative_url }}">the research behind this one</a>.</p>
