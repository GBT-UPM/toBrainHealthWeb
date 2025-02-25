---
layout: default
title: "About Us"
permalink: /aboutus
---

## About Us
<!-- 
Welcome to toBrainHealth, an interdisciplinary collaboration between the Biomedical Engineering and Telemedicine Centre of UPM and the Institut Guttmann Barcelona  brings a holistic approach to brain health. Our primary mission is to promote cerebral well-being while striving for the early diagnosis of neurological and neuropsychiatric conditions. By harnessing the latest advancements in medical science, we tailor cutting-edge techniques to address each individual's unique health challenges. Our specialized, intensive neurorehabilitation programs are person-centered, aiming to restore, enhance, or compensate for functional deficits arising from neurological injuries. At toBrainHealth, we are committed to delivering the highest standard of care for your brain health journey.
-->
Welcome to toBrainHealth, an interdisciplinary collaboration between The Biomedical Engineering and Telemedicine Centre (GBT) at UPM, which is part of the CTB (Center for Biomedical Technology), and Institut Guttmann in Barcelona, offering a holistic approach to brain health. Our primary mission is to promote cerebral well-being and facilitate the early diagnosis of neurological and neuropsychiatric conditions. By leveraging the latest advancements in medical science, we customize cutting-edge techniques to address each individual's unique health challenges. Our specialized, intensive neurorehabilitation programs are person-centered, designed to restore, enhance, or compensate for functional deficits resulting from neurological injuries. At toBrainHealth, we are dedicated to delivering the highest standard of care on your journey toward optimal brain health.

<div style="display: flex;">
  <div style="flex: 50%; padding: 2%;">
    <img src="assets/logos/GBT_SIMPLE.png" alt="Logo GBT" width="65%">
    <img src="assets/logos/ctb.png" alt="Logo CTB" width="65%">
  </div>
  <div style="flex: 50%; padding: 0%;">
    <img src="assets/logos/logo-guttmann.jpg" alt="Logo Guttmann" width="100%">
  </div>
</div>

{% assign alldocs = site.people | sort: "position" %}  

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
