---
layout: page
title: "Notes"
permalink: /notes/
standfirst: >-
  Short pieces on labour markets, data and the things I run into while working. Occasional rather
  than regular.
body_class: ""
description: >-
  Notes by Matías Golman on labour markets, informal employment, skills and working with data.
sitemap: false
---

{%- if site.posts.size > 0 %}
<ul class="entries">
  {%- for post in site.posts %}
  <li class="entry">
    <div class="entry__when">{{ post.date | date: "%b %Y" }}</div>
    <div>
      <h3 class="entry__title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      {%- if post.description %}<p class="entry__text">{{ post.description }}</p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>
{%- else %}
<p>Nothing published here yet.</p>
{%- endif %}
