---
layout: default
title: Home
description: Portfolio of game designer and developer Olawole Abayomi-Owodunni
---

<div class="hero">
    <h1>OLAWOLE ABAYOMI-OWODUNNI</h1>
    <p>Game Designer & Developer</p>
    <p>Creating engaging interactive experiences through thoughtful design and innovative gameplay mechanics.</p>
</div>

<div class="container">
    <h2 class="section-header">ABOUT ME</h2>
    
    <div class="content-panel">
        <p>
            Welcome to my portfolio! I'm a passionate game designer and developer with a focus on creating 
            memorable player experiences. My work spans various genres and platforms, from strategic gameplay 
            to narrative-driven experiences.
        </p>
        <p>
            I believe in the power of games to tell stories, challenge players, and create lasting impressions. 
            Each project in my portfolio represents a commitment to quality design, player engagement, and 
            creative problem-solving.
        </p>
    </div>

    <h2 class="section-header">SKILLS</h2>
    
    <div class="skills-grid">
        <div class="skill-item">Game Design</div>
        <div class="skill-item">Level Design</div>
        <div class="skill-item">Unity</div>
        <div class="skill-item">C# Programming</div>
        <div class="skill-item">Gameplay Systems</div>
        <div class="skill-item">Prototyping</div>
        <div class="skill-item">UX Design</div>
        <div class="skill-item">Project Management</div>
    </div>

    <h2 class="section-header">FEATURED PROJECTS</h2>
    
    <div class="projects-grid">
        {% for project in site.data.projects.published limit:3 %}
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

    <div style="text-align: center; margin-top: 2rem;">
        <a href="{{ '/projects/' | relative_url }}" class="btn">View All Projects</a>
    </div>
</div>
