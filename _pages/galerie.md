---
title: "Meine Gitarren"
permalink: /gitarren/
layout: single
author_profile: true
---

Hier stelle ich meine abgeschlossenen und laufenden Gitarrenbau-Projekte vor.

<div class="guitar-grid">

{% assign guitars = site.guitars | sort: "build_year" | reverse %}

{% for guitar in guitars %}

  {{ guitar.url | relative_url }}

    {% if guitar.cover_image %}
      {{ guitar.cover_image | relative_url }}
    {% endif %}

    <div class="guitar-card-content">

      <h2>{{ guitar.title }}</h2>

      {% if guitar.guitar_type %}
        <p class="guitar-type">{{ guitar.guitar_type }}</p>
      {% endif %}

      {% if guitar.build_year %}
        <p class="guitar-year">Baujahr {{ guitar.build_year }}</p>
      {% endif %}

    </div>

  </a>

{% endfor %}

</div>
