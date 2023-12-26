---
title: "배운 것 적용해보기"
layout: archive
permalink: /implement
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['implement']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}