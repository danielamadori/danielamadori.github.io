---
permalink: /de/publications/
lang: de
pid: publications
title: "Veröffentlichungen"
layout: archive
author_profile: true
---

{% if author.googlescholar %}
  Meine Artikel finden Sie auch auf <u><a href="{{author.googlescholar}}">meinem Google-Scholar-Profil</a>.</u>
{% endif %}

{% include base_path %}

{% include experience-timeline.html from="2025-07" flat="true" %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
