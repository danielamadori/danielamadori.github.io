---
permalink: /it/publications/
lang: it
pid: publications
title: "Pubblicazioni"
layout: archive
author_profile: true
---

{% if author.googlescholar %}
  Trovi i miei articoli anche su <u><a href="{{author.googlescholar}}">il mio profilo Google Scholar</a>.</u>
{% endif %}

{% include base_path %}

{% include experience-timeline.html from="2025-07" %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
