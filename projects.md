---
layout: default
title: Projects
description: Explore my game design and development projects
permalink: /projects/
---

<div class="container">
    <h1 class="section-header">GAMES</h1>

    <!-- Published Projects -->
    <h2>Published</h2>
    <div class="projects-grid">
        {% for project in site.data.projects.published %}
        <a href="{{ '/projects/' | append: project.slug | append: '/' | relative_url }}" class="project-card">
            <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }}" class="project-card-image">
            <div class="project-card-content">
                <div class="project-card-meta">{{ project.category }}</div>
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
            </div>
        </a>
        {% endfor %}
    </div>

    <!-- School Projects -->
    <h2>School Projects</h2>
    <div class="projects-grid">
        {% for project in site.data.projects.school %}
        <a href="{{ '/projects/' | append: project.slug | append: '/' | relative_url }}" class="project-card">
            <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }}" class="project-card-image">
            <div class="project-card-content">
                <div class="project-card-meta">{{ project.category }}</div>
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
            </div>
        </a>
        {% endfor %}
    </div>

    <!-- Personal Projects -->
    <h2>Personal Projects</h2>
    <div class="projects-grid">
        {% for project in site.data.projects.personal %}
        <a href="{{ '/projects/' | append: project.slug | append: '/' | relative_url }}" class="project-card">
            <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }}" class="project-card-image">
            <div class="project-card-content">
                <div class="project-card-meta">{{ project.category }}</div>
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
                {% if project.coming_soon %}
                <p><em>Coming Soon</em></p>
                {% endif %}
            </div>
        </a>
        {% endfor %}
    </div>
</div>
