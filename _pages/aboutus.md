---
layout: default
title: "About Us"
permalink: /aboutus
---

## About Us

Welcome to ToBrainHealth, where a collaboration between the experts at Guttmann Barcelona and the innovative minds of the Bioengineering and Telemedicine Group at UPM brings you a holistic approach to brain health. Our primary mission is to promote cerebral well-being while striving for the early diagnosis of neurological and neuropsychiatric conditions. By harnessing the latest advancements in medical science, we tailor cutting-edge techniques to address each individual's unique health challenges. Our specialized, intensive neurorehabilitation programs are person-centered, aiming to restore, enhance, or compensate for functional deficits arising from neurological injuries. At ToBrainHealth, we are committed to delivering the highest standard of care for your brain health journey.

<div style="display: flex;">
  <div style="flex: 50%; padding: 3.5%;">
    <img src="assets/logos/GBT_SIMPLE.png" alt="Logo GBT" width="65%">
  </div>
  <div style="flex: 50%; padding: 5%;">
    <img src="assets/logos/logo-guttmann.jpg" alt="Logo Guttmann" width="100%">
  </div>
</div>

## People

{% assign alldocs = site.people | sort: 'name' %}  

<div class="card-deck">
{% for author in alldocs %}
  <div class="card mb-4">
    <div class="row">
      <div class="col-md-6">
        <img src="{{ author.image }}" class="card-img-top" alt="Imagen de la Tarjeta">
      </div>
    <div class="col-md-6">
      <div class="card-body">
        <h5 class="card-title">{{ author.title }}</h5>
        <h6 class="card-subtitle">{{ author.subtitle }}</h6>
        <p class="card-text">{{ author.description }}</p>
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



<!--
<div class="card-container">
  {% for author in site.people %}
    <div class="card">
      <img src="{{author.image}}">
      <h2>{{ author.title }}</h2>
      <h3>{{ author.subtitle }}</h3>
      <p>{{ author.content | markdownify }}</p>
    </div>
  {% endfor %}
</div>-->