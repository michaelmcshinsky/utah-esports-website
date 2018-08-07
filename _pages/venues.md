---
layout: default
title: Venues and Vendors
permalink: /venues
---

<div style="max-width: 1200px;margin: 50px auto;padding: 0 30px;">
  <div class="heading" style="margin: 50px 0 0">
    <h1>
      {{ page.title }}
    </h1>
  </div>
  <hr/>
  <div class="row">
    {% for venue in site.data.venues %}
      <div class="col-xs-6 col-sm-4" style="margin-top: 50px;">
        <img src="/assets/images/vendors/{{ venue.image }}.png" alt="{{ venue.name }}"/>
        <h3 style="margin-top: 15px;">{{ venue.name }}</h3>
        {% if venue.url %}
          <div><a href="{{ venue.url }}" target="_blank">Website</a></div>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</div>

<style>
  .col-xs-6 a {
    color: #fff;
    font-size: 14px;
  }
  .col-xs-6 a:hover {
    color: #FF290F;
  }
  .col-xs-6 img {
    border: 1px solid #2d313a;
  }
</style>