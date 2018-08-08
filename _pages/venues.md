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
  <p>We love supporting the local community and the venues&amp; vendors that make it possible. Below are a great sample of businesses out there who are striving to make sure Utah's Esports scene is and stays on the map!<br/>Don't see your business listed here? Let us Know! Send us a message at: <a href="mailto:info@utahesports.net">info@utahesports.net</a>.</p>
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
    color: #03A9F3;
  }
  .col-xs-6 img {
    border: 1px solid #2d313a;
  }
</style>