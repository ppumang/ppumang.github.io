---
title: "team"
layout: archive
permalink: /team
author_profile: true
---


{% assign posts = site.categories.team %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
