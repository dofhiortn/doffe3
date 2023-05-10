---
layout: songs
title: Songs
permalink: /songs/
---

<ul>
{% for song in site.songs %}
    <li>
    <a href="{{site.baseurl}}{{song.url}}">{{song.title}}</a>
    </li>

{% endfor %}
</ul>