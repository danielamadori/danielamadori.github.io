---
permalink: /de/sitemap/
lang: de
pid: sitemap
title: "Seitenübersicht"
layout: archive
author_profile: true
sitemap: false
---

{% include base_path %}

Eine Liste aller Seiten und Beiträge dieser Website. Für Maschinen steht auch eine [XML-Fassung]({{base_path}}/sitemap.xml) bereit.

<h2>Pages</h2>
{% for post in site.pages %}{% if post.lang == page.lang %}
  {% include archive-single.html %}
{% endif %}{% endfor %}

<!--
For remove pages from sitemap

<h2>Posts</h2>
{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% unless collection.output == false or collection.label == "posts" %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}

-->