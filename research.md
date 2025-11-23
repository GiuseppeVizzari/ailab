---
layout: default
title: Research
permalink: /research/
---

<div class="container">
    <h1>Research</h1>

    <h2>Research Lines</h2>
    <div class="post-list">
        {% for line in site.data.research_lines %}
        <div class="post-card">
            <h3>{{ line.title }}</h3>
            <p>{{ line.description }}</p>
        </div>
        {% endfor %}
    </div>

    <h2 style="margin-top: 60px;">Ongoing Projects</h2>
    <div class="post-list">
        {% assign ongoing_projects = site.projects | where: "status", "ongoing" %}
        {% for project in ongoing_projects %}
        <div class="post-card">
            <h3>{{ project.title }}</h3>
            <p class="post-meta">Funded by: {{ project.funding_agency }}</p>
            <p>{{ project.description }}</p>
        </div>
        {% endfor %}
    </div>

    <h2 style="margin-top: 60px;">Past Projects</h2>
    <div class="post-list">
        {% assign past_projects = site.projects | where: "status", "past" %}
        {% for project in past_projects %}
        <div class="post-card">
            <h3>{{ project.title }}</h3>
            <p class="post-meta">Funded by: {{ project.funding_agency }}</p>
            <p>{{ project.description }}</p>
        </div>
        {% endfor %}
    </div>
</div>
