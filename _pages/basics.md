---
title: "논문을 이해하기 위해 필요한 기초 수학"
layout: archive
permalink: /basics
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['basics']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}