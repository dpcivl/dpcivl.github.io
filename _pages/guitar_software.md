---
title: "소프트웨어 관련"
layout: archive
permalink: /guitar/software
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['software']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}