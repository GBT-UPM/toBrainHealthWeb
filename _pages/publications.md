---
layout: default
title: "Publications"
permalink: /publications
---

{% assign alldocs = site.publications | sort: "position" %}  

<div style="display: flex;">
  <div style="flex: 50%;padding-right:3%">

{% for author in alldocs %}
  {% if author.institution == "GBT" %}
  <div class="row mb-4">
    <div class="card">
        <img src="{{ author.image }}" class="card-img" alt="Imagen de la Tarjeta" style="margin-top:10px">
      <div class="card-body">
        <h5 class="card-title">{{ author.title }}
          {% if author.orcid_url %}
            <a href="{{ author.orcid_url }}" target="_blank"><i class="fa-brands fa-orcid"></i></a>
          {% endif %}
        </h5>
        <p class="card-text">{{ author.subtitle }}</p>
        <div class="collapse" id="collapse{{ forloop.index }}">
          <p>{{ author.content }}</p>
        </div>
        <a class="btn btn-primary" data-toggle="collapse" href="#collapse{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ forloop.index }}">
          Read more
        </a>
      </div>
    </div>
    </div>
    {% endif %}
 {% endfor %}
  </div>
    <div style="flex: 50%;padding-left:3%">

{% for author in alldocs %}
  {% if author.institution == "Guttmann" %}
  <div class="row mb-4">
    <div class="card">
        <img src="{{ author.image }}" class="card-img" alt="Imagen de la Tarjeta" style="margin-top:10px">
      <div class="card-body">
        <h5 class="card-title">{{ author.title }}
          {% if author.orcid_url %}
            <a href="{{ author.orcid_url }}" target="_blank"><i class="fa-brands fa-orcid"></i></a>
          {% endif %}
        </h5>
        <p class="card-text">{{ author.subtitle }}</p>
        <div class="collapse" id="collapse{{ forloop.index }}">
          <p>{{ author.content }}</p>
        </div>
        <a class="btn btn-primary" data-toggle="collapse" href="#collapse{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ forloop.index }}">
          Read more
        </a>
      </div>
    </div>
    </div>
    {% endif %}
 {% endfor %}
  </div>
</div>
