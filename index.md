---
layout: default
title: Home
description: Portfolio of game designer and developer Olawole Abayomi-Owodunni

# Featured games - Type 1 (video showcase, 30/70 split)
# Just add the project slug here to feature it
featured_showcase:
  - operation-reclaim
  - experiment-vessel

# Featured games - Type 2 (image card grid, 3 columns)
# Just add the project slug here to feature it
featured_cards:
  - olis-cofferia
  - wisteria
---

<div class="hero">
    <h1>OLAWOLE ABAYOMI-OWODUNNI</h1>
    <h2>GAME DESIGNER</h2>
    <p>Hi there! My name is Olawole, a 4th year Game Designer studying Computer Games Development at SETU Carlow. I am super passionate about crafting worlds and experiences focused and designed around the player.</p>
    <p>Welcome to my Portfolio Site detailing my experience and work.</p>
</div>

<div class="container">
    <h2 class="section-header">FEATURED GAMES</h2>
    {% for slug in page.featured_showcase %}
        {% assign project = null %}
        {% for p in site.data.projects.published %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
        {% for p in site.data.projects.school %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
        {% for p in site.data.projects.personal %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
        {% if project %}
    <div class="game-showcase">
        <div class="game-showcase-video">
            <div class="video-wrapper">
                <iframe 
                    src="https://www.youtube.com/embed/{{ project.youtube_id }}" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen>
                </iframe>
            </div>
        </div>
        <div class="game-showcase-info">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <a href="{{ '/projects/' | append: project.slug | append: '/' | relative_url }}" class="btn-showcase">Click here for project page</a>
        </div>
    </div>
        {% endif %}
    {% endfor %}

    <div class="game-cards-grid">
        {% for slug in page.featured_cards %}
            {% assign project = null %}
            {% for p in site.data.projects.published %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
            {% for p in site.data.projects.school %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
            {% for p in site.data.projects.personal %}{% if p.slug == slug %}{% assign project = p %}{% endif %}{% endfor %}
            {% if project %}
        <div class="game-card">
            <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }}" class="game-card-image">
            <div class="game-card-content">
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
                <a href="{{ '/projects/' | append: project.slug | append: '/' | relative_url }}" class="btn-showcase">Click here for project page</a>
            </div>
        </div>
            {% endif %}
        {% endfor %}
    </div>

    <div style="text-align: center; margin-top: 2rem;">
        <a href="{{ '/projects/' | relative_url }}" class="btn">View All Projects</a>
    </div>
    <div class="about-section">
        <div class="about-top">
            <div class="about-left">
                <h2 class="section-header">ABOUT ME</h2>
                <div class="about-portrait-wrapper">
                    <img src="/assets/img/portrait.png" alt="Olawole Abayomi-Owodunni" class="about-portrait">
                </div>
            </div>
            <div class="about-right">
                <p>
                    A Game Designer born and raised in the heart of Lagos, Nigeria. I have been a passionate gamer since the tender age of 5 and a passionate Game Designer since I discovered it was a viable career path in 2019. I am inspired by games like <em>Lies of P</em> for its finely tuned combat mechanics, <em>Hollow Knight</em> for its excellence in level design and sense of discovery and <em>The Outer Worlds</em> for its deep characters and immersive RPG mechanics.
                </p>
                <p>
                    My journey in game development started in the summer of 2019 with my <strong>internship as a Game Designer</strong> at 9ijakids games where I learned the most basic tools of the trade from, <strong>conceptualization</strong> and <strong>documentation</strong> to the importance of <strong>design iteration</strong>. After the internship was over, I was curious to discover more of what making games was all about which lead me to YouTube channels and courses dedicated on teaching how to make games and the fundamentals of game design. However, it wasn't until I started making games myself that I fell in love with game design. Everything from designing mechanics and iterating based on playtests to the satisfaction of seeing your game in the hands of the people you painstakingly crafted it for has had me hooked ever since.
                </p>
            </div>
        </div>
        <div class="about-bottom">
            <p>
                Currently I'm studying <strong>Computer Games Development</strong> at South Eastern Technological University - Carlow where I'm learning more <strong>technical tools</strong> of the trade while still <strong>self teaching</strong> myself more of the intricacies of game design through <strong>books</strong> written by reputable <strong>game designers</strong> and YouTube retrospectives on successful and unsuccessful games to learn what works, what doesn't and why.
            </p>
            <p>
                Growing up, I was shaped by a lot of the games I played. Friendly competition with games like FIFA, pushing through adversity with games like Dark Souls, the thrill of exploration with games like Road Trip Adventure. Developers from my childhood had such a massive impact on my life and overall development.
            </p>
            <p>
                That's why I make games. To craft memorable and impactful experiences for gamers, just like developers before did for me. <strong>For Players, By a Player.</strong>
            </p>
        </div>
        <div class="about-cta">
            <a href="/resume/" class="btn-showcase">Click here to view my resume</a>
        </div>
    </div>
</div>
