---
layout: default
title: GitHub Pages Starter
permalink: /
---

<div class="page-header">
  <h1 class="page-heading">{{site.custom_settings.name}}</h1>
  <p class="page-tagline">{{site.custom_settings.description}}</p>
</div>

<hr>

{% for partner in site.data.partners %}

<div class="partner-card">
  <div class="text-container">
    <h2>{{ partner.name }}</h2>
    <p class="primary-service">{{ partner.primaryService }}</p>
    <p class="url">{{ partner.url }}</p>
    <p class="description">{{ partner.description }}</p>
    <ul class="services-list">
      {% for service in partner.services %}
      <li>{{ service }}</li>
      {% endfor %}
    </ul>
  </div>
  <div class="image-container">
    <img src="{{ partner.logo.src }}" alt="{{ partner.logo.alt }}">
  </div>
</div>

{% endfor %}