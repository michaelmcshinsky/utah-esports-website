---
title: 
layout: landing
permalink: /
---

<!-- Required Core Stylesheet -->
<link rel="stylesheet" href="https://unpkg.com/@glidejs/glide@3.2.2/dist/css/glide.core.min.css">

<!-- Optional Theme Stylesheet -->
<link rel="stylesheet" href="https://unpkg.com/@glidejs/glide@3.2.2/dist/css/glide.theme.min.css">

{% assign featured_count = 0 %}
<div class="banner-grid">
<div class="featured-events glide">
  <div class="glide__track" data-glide-el="track">
    <ul class="glide__slides">
      {% assign featuredCurDate = site.time | date: '%s' %}
      {% for event in site.events %}
        {% assign featuredStartDate = event.start_date | date: '%s' %}
        {% if featuredStartDate >= featuredCurDate and event.featured == true %}
          {% assign featured_count = featured_count | plus: 1 %}
          <li class="glide__slide">
            <div class="featured">
              <i class="fa fa-star"></i>
              <span>Featured</span>
            </div>
            <img src="{{ event.event_image }}" alt="{{ event.title }}"/>
            <div class="title">
              <a href="{{ event.url }}">{{ event.title }}</a>
            </div>
            <div class="date">
              <span class="month">{{ event.start_date | date: "%B" }}</span>
              <span class="day">{{ event.start_date | date: "%d" }},</span>
              <span class="year">{{ event.start_date | date: "%Y" }}</span>
            </div>
          </li>
        {% endif %}
      {% endfor %}
    </ul>
  </div>
  {% if featured_count > 1 %}
  <div class="glide__arrows" data-glide-el="controls">
    <button class="glide__arrow glide__arrow--left" data-glide-dir="<">prev</button>
    <button class="glide__arrow glide__arrow--right" data-glide-dir=">">next</button>
  </div>
  {% endif %}
</div>

<!-- <img src="/assets/images/home/utah-esports-banner-7.jpg" alt="banner"/> -->

<div class="heading" style="margin-top: 0;">
  <h3>
    Upcoming Events
    <a href="/calendar" class="btn btn--default">View All Events</a>
    <span>/ </span><a href="/submit-event" class="btn btn--default">Submit Event</a>
  </h3>
  <!-- <div class="pull-right">
    <a href="https://docs.google.com/forms/d/e/1FAIpQLSd_Nj2QKQTkN3NzUCnQKX7YlLM1Avt_jDOhqVxg3xXlrv5ytg/viewform?usp=sf_link" class="btn btn--primary" target="_blank">Submit Event</a>
  </div> -->
</div>
<ul class="event-list">
{% assign counter = 0 %}
{% assign curDate = site.time | date: '%s' %}
{% for event in site.events %}
  {% assign eventStartDate = event.start_date | date: '%s' %}
  {% if eventStartDate >= curDate and counter < 4 %}
    {% assign counter = counter | plus: 1 %}
    <li class="event-item">
      <div class="event-image">
        <img src="{{ event.event_image }}" alt="{{ event.title }}"/>
      </div>
      <div class="event-content">
        <div class="title">
          <a href="{{ event.url }}">{{ event.title }}</a>
        </div>
        <!-- <div class="excerpt">{{ event.excerpt | strip_html | truncatewords: 20 }}</div> -->
        <div class="event-meta">
          <div class="date">
            <span class="day">{{ event.start_date | date: "%d" }}</span>
            <span class="month">{{ event.start_date | date: "%b" }}</span>
            <span class="year">{{ event.start_date | date: "%Y" }}</span>
          </div>
          <div class="link"><a href="{{ event.url }}">View Event</a></div>
        </div>
      </div>
    </li>
  {% endif %}
{% endfor %}
</ul>
<div style="margin-top: 25px">
  <img src="http://via.placeholder.com/1200x150/111111/cccccc?text=Your+Ad+Here" alt="ad">
</div>

<div class="heading" style="margin-top: 1em;">
  <h3>
    The Community
    <a class="btn btn--default">&zwnj;</a>
  </h3>
</div>

<div class="row">
  <div class="col-xs-12 col-sm-4 col-md-4">
    <div class="card">
      <div class="card-image">
        <img src="/assets/images/home/teams-and-clubs.jpg" alt="Teams and Clubs" style="width:100%;"/>
        <div class="card-image-title">
          <h3>Teams &amp; Clubs <a class="btn btn--primary" href="/teams-and-clubs">See More</a></h3>
        </div>
      </div>
    </div>
  </div>
  <div class="col-xs-12 col-sm-4 col-md-4">
    <div class="card">
      <div class="card-image">
        <img src="/assets/images/home/streams-and-videos.jpg" alt="Streams and Videos" style="width:100%;"/>
        <div class="card-image-title">
          <h3>Streams &amp; Videos <a class="btn btn--primary" href="/streams">See More</a></h3>
        </div>
      </div>
    </div>
  </div>
  <div class="col-xs-12 col-sm-4 col-md-4">
    <div class="card">
      <div class="card-image">
        <img src="/assets/images/home/social-groups.jpg" alt="Social Groups" style="width:100%;"/>
        <div class="card-image-title">
          <h3>Social Groups <a class="btn btn--primary" href="/social-groups">See More</a></h3>
        </div>
      </div>
    </div>
  </div>
</div>

<script type="text/javascript" src="https://unpkg.com/@glidejs/glide@3.2.2/dist/glide.min.js"></script>
<script>
  document.onreadystatechange = function () {
      if (document.readyState == "interactive") {
        new Glide('.glide', {
          type: 'carousel',
          startAt: 0,
          perView: 1
        }).mount()
      }
  }
</script>