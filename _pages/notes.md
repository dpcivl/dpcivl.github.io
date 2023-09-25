---
title: "Notes for learning"
layout: archive
permalink: /notes
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['notes']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}