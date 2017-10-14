---
layout: archive
title: "Professional Activities"
permalink: /professional/
author_profile: true
---

{% include base_path %}

{% assign current_year = "" %}
{% for post in site.professional reversed %}
  {% assign year = post.date | date: "%Y" %}
  {% if current_year != year %}
    {% assign current_year = year %}
    {% include archive-subheader.html %}
  {% endif %}
  {% include archive-single-professional.html %}
{% endfor %}
