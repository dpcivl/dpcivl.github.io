---
title: "기타 다른 공부"
layout: archive
permalink: /guitar
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['guitar']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}