---
title: Noticias
layout: page
permalink: /noticias
---

<div class="container my-4 posts">
  <h1>Reseñas</h1>
  <p>{{ site.description }}</p>

  <!-- Blog Posts Section -->
  <div class="row">
    {% for post in site.posts %}
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="{{ post.thumbnail | relative_url }}" class="card-img-top" alt="Imagen de la reseña">
          <div class="card-body">
            <h5 class="card-title">
              <a href="{{ post.url | relative_url }}" class="card-link">{{ post.title }}</a>
            </h5>
            <h6>Por: {{post.author}}</h6>
            <p class="meta">
              <button class="btn btn-secondary btn-sm" disabled>Publicado el {{ post.date | date: "%d/%m/%Y" }}</button>
            </p>
            <p class="card-text">{{ post.excerpt }}</p>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
