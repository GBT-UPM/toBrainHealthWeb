---
layout: default
title: "Publications"
permalink: /publication
---

{% assign alldocs = site.publications | sort: "position" %}  

<div style="display: flex;">

{% for publication in alldocs %}
  <div class="row mb-4">
    <div class="card">
        <img src="{{ publication.image }}" class="card-img" alt="Imagen de la Tarjeta" style="margin-top:10px">
      <div class="card-body">
        <h5 class="card-title">{{ publication.title }}</h5>
        <h5 class="card-subtitle">{{ publication.authors }}</h5>
        {% if publication.doi %}
        <h5 class="card-subtitle">{{ publication.doi }}</h5>
        {% endif %}
        <p class="card-text">{{ publication.abstract }}</p>
        <div class="collapse" id="collapse{{ forloop.index }}">
          <p>{{ author.content }}</p>
        </div>
        <a class="btn btn-primary" data-toggle="collapse" href="#collapse{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ forloop.index }}">
          Read more
        </a>
      </div>
    </div>
    </div>
 {% endfor %}
  </div>
</div>
