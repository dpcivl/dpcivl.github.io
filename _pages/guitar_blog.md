---
title: "깃허브 블로그 설정 관련"
layout: archive
permalink: /guitar/blog
author_profile: true
types: posts
sidebar:
    nav: "docs"
---

{% assign posts = site.categories['blog']%}
{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}