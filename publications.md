---
layout: default
title: Publications
permalink: /publications/
---

<div class="container">
    <h1>Publications</h1>
    <ul class="post-list">
        {% for pub in site.data.publications %}
        <li class="post-card">
            <h3><a href="{{ pub.link }}" target="_blank">{{ pub.title }}</a></h3>
            <p>{{ pub.authors }}</p>
            <p class="post-meta">{{ pub.venue }}, {{ pub.year }}</p>
        </li>
        {% endfor %}
    </ul>
</div>
