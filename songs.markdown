---
layout: songs
title: Songs
permalink: /songs/
---

<ul>
{% for song in site.songs %}
    <li>
    {%- if song.artwork -%}
    <img src="{{site.baseurl}}/assets/img/{{song.artwork}}" alt='Artwork for "{{song.title}}"' class="artwork" />
    {%- endif -%}
    <a href="{{site.baseurl}}{{song.url}}">{{song.title}}</a>
    </li>

{% endfor %}
</ul>