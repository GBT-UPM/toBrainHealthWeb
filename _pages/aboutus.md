---
layout: default
title: "About Us"
permalink: /aboutus
---

## About Us

Welcome to ToBrainHealth, where a collaboration between the experts at Guttmann Barcelona and the innovative minds of the Bioengineering and Telemedicine Group at UPM brings you a holistic approach to brain health. Our primary mission is to promote cerebral well-being while striving for the early diagnosis of neurological and neuropsychiatric conditions. By harnessing the latest advancements in medical science, we tailor cutting-edge techniques to address each individual's unique health challenges. Our specialized, intensive neurorehabilitation programs are person-centered, aiming to restore, enhance, or compensate for functional deficits arising from neurological injuries. At ToBrainHealth, we are committed to delivering the highest standard of care for your brain health journey.

<div style="display: flex;">
  <div style="flex: 50%; padding: 2%;">
    <img src="assets/logos/GBT_SIMPLE.png" alt="Logo GBT" width="65%">
  </div>
  <div style="flex: 50%; padding: 0%;">
    <img src="assets/logos/logo-guttmann.jpg" alt="Logo Guttmann" width="100%">
  </div>
</div>

{% assign alldocs = site.people | sort: "position" %}  

<div style="display: flex;">
  <div style="flex: 50%; padding: 3.5%;">

{% for author in alldocs %}
  {% if author.institution == "GBT" %}
    <div class="card">
        <img src="{{ author.image }}" class="card-img-top" alt="Imagen de la Tarjeta">
      <div class="card-body">
        <h5 class="card-title">{{ author.title }}</h5>
        <p class="card-text">{{ author.subtitle }}</p>
        <div class="collapse" id="collapse{{ forloop.index }}">
          <p>{{ author.content }}</p>
        </div>
        <a class="btn btn-primary" data-toggle="collapse" href="#collapse{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ forloop.index }}">
          Read more
        </a>
      </div>
    </div>
    {% endif %}
 {% endfor %}
  </div>
    <div style="flex: 50%; padding: 3.5%;">

{% for author in alldocs %}
  {% if author.institution == "Guttmann" %}
    <div class="card">
        <img src="{{ author.image }}" class="card-img-top" alt="Imagen de la Tarjeta">
      <div class="card-body">
        <h5 class="card-title">{{ author.title }}</h5>
        <p class="card-text">{{ author.subtitle }}</p>
        <div class="collapse" id="collapse{{ forloop.index }}">
          <p>{{ author.content }}</p>
        </div>
        <a class="btn btn-primary" data-toggle="collapse" href="#collapse{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ forloop.index }}">
          Read more
        </a>
      </div>
    </div>
    {% endif %}
 {% endfor %}
  </div>
</div>
