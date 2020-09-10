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

<p>Popular Demand, LLC is a starting point for innovators, businesses, and entrepreneurs to find the right solutions for their next venture. We are innovators, business, and entrepreneurs ourselves; what we love to do is <b>CREATE!</b></p>
<p>If you're looking for a builder/designer/consultation for your next project, find just the one you need from our partners.</p>
<p>If you are an innovation-minded builder, join our community. We are looking for <b>all types of creators</b> — artists, writers, videographers, software, hardware, welders... If you can create a new thing from simply an idea, we'd love to talk, get you fit in, and connect you with people who could use your services.</p>
<p>Get in Touch! <a href="mailto:team@popdemtech.com">team@popdemtech.com</a></p>

<hr>

<h2>Our Partners</h2>
{% for partner in site.data.partners %}

<div class="partner-card">
  <div class="text-container">
    <h3>{{ partner.name }}</h3>
    <div class="meta">
      <p class="primary-service"><b>Service:</b> {{ partner.primaryService | capitalize }}</p>
      <p class="url"><b>Website:</b> <a href="{{ partner.url }}">{{ partner.url }}</a></p>
      <p class="url"><b>Contact:</b> <a href="{{ partner.url }}">{{ partner.email }}</a></p>
    </div>
    <p class="description">{{ partner.description }}</p>
    <ul class="services-list">
      {% for service in partner.services %}
      <li>{{ service | capitalize }}</li>
      {% endfor %}
    </ul>
  </div>
  <div class="image-container">
    <img src="{{ partner.logo.src }}" alt="{{ partner.logo.alt }}">
  </div>
</div>

{% endfor %}