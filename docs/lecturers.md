---
layout: default
permalink: /lecturers/
title: Lecturers
hero:
  image: "/assets/img/heros/Feynman-diagram.webp"  # Optional
  title: "Lecturers"
---
# Lecturers

<div class="grid grid-2">
  {% for p in site.data.lecturers %}
    {% assign photo = p.photo | default: '/assets/img/default-lecturer.svg' %}
    <div class="card">
      <img src="{{photo | relative_url}}" alt="{{p.name}}" style="width:100%;max-height:220px;object-fit:cover;border-radius:8px;margin-bottom:.5rem">
      <h3 style="margin:.2rem 0">{{p.name}}</h3>
      <div style="color:#666;margin:0.5rem 0; line-height:1.2">{{p.affiliation}}</div>
      <div style="color:#666;margin:-0.5rem 0">{{p.email}}</div>
      <p style="margin-top:.75rem">{{p.intro}}</p>
    </div>
  {% endfor %}
</div>
