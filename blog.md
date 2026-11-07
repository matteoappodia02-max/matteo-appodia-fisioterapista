---
layout: default
title: "Blog & Approfondimenti | Matteo Appodia"
permalink: /blog/
---

<div class="section section-light">
    <div class="container">
        <h1 style="color: var(--primary); text-align: center; margin-bottom: 20px;">Tutti gli articoli</h1>
        <p style="text-align: center; color: #64748b; margin-bottom: 50px;">Approfondimenti su fisioterapia, gestione del dolore e recupero dell'autonomia.</p>
      <div class="grid">
            {% for post in site.posts %}
            <div class="blog-card">
                {% if post.image %}
                <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
                {% endif %}
                <div class="blog-content">
                    <span class="date">{{ post.date | date: "%d/%m/%Y" }}</span>
                    <h3>{{ post.title }}</h3>
                    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
                    <a href="{{ post.url | relative_url }}" class="read-more">Leggi articolo &rarr;</a>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>
</div>
