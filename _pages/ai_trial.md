---
title: "AI 관련 구현 과정 정리"
layout: archive
permalink: /ai/trial
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['ai/trial']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}