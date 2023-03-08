---
layout: home
---

# Upcoming shows
{% assign today = site.time | date: "%Y-%m-%d" %}
{% assign future_dates_found = false %}
{% for event in site.data.shows %}

  {% assign event_date = event.date | date: "%Y-%m-%d" %}

  {% if event_date >= today %}
  {% assign future_dates_found = true %}
- {{ event.date | date: "%Y-%m-%d" }} - {{ event.event }} - {{ event.place }}
  {% endif %}

{% endfor %}

{% if future_dates_found == false %}
  <p>No future dates.</p>
{% endif %}