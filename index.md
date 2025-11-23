---
layout: default
title: Home
description: Welcome to the AILAB.
---

<section class="hero">
    <div class="container">
        <h1>Welcome to AILAB</h1>
        <p class="lead">Exploring the frontiers of Artificial Intelligence.</p>
        <a href="{{ "/about" | relative_url }}" class="btn">Learn More</a>
    </div>
</section>

<section class="latest-posts container">
    <h2 style="text-align: center; margin-bottom: 40px; font-size: 2rem;">Latest Updates</h2>
    <ul class="post-list">
        {% for post in site.posts %}
        <li class="post-card">
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            <h3>
                <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            </h3>
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        </li>
        {% endfor %}
    </ul>
</section>
