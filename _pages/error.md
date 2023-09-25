---
title: "How I solved error"
layout: archive
permalink: /error
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['error']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}