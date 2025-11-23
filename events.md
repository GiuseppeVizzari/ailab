---
layout: default
title: Events
permalink: /events/
---

<div class="container">
    <h1>Events</h1>
    <ul class="post-list">
        {% for event in site.events %}
        <li class="post-card">
            <span class="post-meta">{{ event.date | date: "%b %-d, %Y" }} | {{ event.type }}</span>
            <h3>{{ event.title }}</h3>
            <p><strong>Location:</strong> {{ event.location }}</p>
            <p>{{ event.content | strip_html | truncatewords: 30 }}</p>
        </li>
        {% endfor %}
    </ul>
</div>
