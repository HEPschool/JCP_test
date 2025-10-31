---
layout: default
permalink: /schedule/
title: Schedule
hero:
  image: "/assets/img/heros/Feynman-diagram.webp"  # Optional
  title: "Schedule"
---
# Schedule

You can view the details of each lecture/special talk by clicking on it.

<table>
<thead>
  <tr><th>Date/Time</th><th>Title</th><th>Speaker</th><th>Location</th><th>Note</th></tr>
</thead>
<tbody>
{% assign all = site.events | sort: 'date' %}
{% for ev in all %}
<tr onclick="location.href='{{ ev.url | relative_url }}'" style="cursor:pointer">
  <td>{{ ev.date | date: "%Y-%m-%d %H:%M" }}</td>
  <td>{{ ev.title }}</td>
  <td>{{ ev.speaker | default: "TBD" }}</td>
  <td>{{ ev.location }}</td><td>{{ ev.note | default: '' }}</td>
</tr>
{% endfor %}
</tbody>
</table>
