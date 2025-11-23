---
layout: default
title: People
permalink: /people/
---

<div class="container">
    <h1>People</h1>

    <h2>Current Members</h2>
    <div class="post-list">
        {% assign current_people = site.people | where: "status", "current" %}
        {% for person in current_people %}
        <div class="post-card">
            <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 100px; height: 100px; border-radius: 50%; margin-bottom: 15px;">
            <h3>{{ person.name }}</h3>
            <p class="post-meta">{{ person.role }}</p>
            <p>{{ person.bio }}</p>
        </div>
        {% endfor %}
    </div>

    <h2 style="margin-top: 60px;">Alumni</h2>
    <ul class="post-list">
        {% assign alumni = site.people | where: "status", "alumni" %}
        {% for person in alumni %}
        <li class="post-card">
            <h3>{{ person.name }}</h3>
            <p class="post-meta">{{ person.role }}</p>
            <p>{{ person.bio }}</p>
        </li>
        {% endfor %}
    </ul>
</div>
