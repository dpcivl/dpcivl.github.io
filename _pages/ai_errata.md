---
title: "AI 관련 에러 해결"
layout: archive
permalink: /ai/errata
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['ai_errata']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}