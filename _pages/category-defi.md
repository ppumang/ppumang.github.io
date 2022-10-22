---
title: "defi"
layout: archive
permalink: /defi
author_profile: true
---

{% assign posts = site.categories.defi %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
