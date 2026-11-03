---
permalink: /en/publications/
lang: en
pid: publications
layout: archive
title: "Publications"
author_profile: true
redirect_from:
  - /publications/
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% include experience-timeline.html from="2025-07" %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
