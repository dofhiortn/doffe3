---
layout: page
title: Shows
permalink: /shows/
---

{% assign shows_by_year = site.data.shows | group_by_exp: 'show', 'show.date | date: "%Y"' %}

{% for shows_in_year in shows_by_year %}
## {{ shows_in_year.name }}
{% for show in shows_in_year.items %}
- {{ show.date | date: "%-d %b" }}: {{ show.place }} / {{ show.event }}
{% endfor %}

{% endfor %}