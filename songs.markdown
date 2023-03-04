---
layout: page
title: Songs
permalink: /songs/
---

{% for song in site.songs %}
- [{{song.title}}]({{ song.url | prepend: site.baseurl }})
{% endfor %}
