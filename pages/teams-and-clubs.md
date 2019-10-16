---
layout: default
title: Teams and Clubs
header:
  teaser: "/assets/images/site/logo-square.png"
permalink: /teams-and-clubs
---

<div style="max-width: 1200px;margin: 50px auto;padding: 0 30px;">
  <div class="heading" style="margin: 50px 0 0">
    <h1>
      {{ page.title }}
    </h1>
  </div>
  <p>Local Utah Esports and Gaming communities are on the rise gaining more popularity and success each year. We even have our own Jazz Esports Team! Be sure to support all the local teams and look out for <a href="/events">events</a> where they will go head to head to see who really is the best.<br/>Don't see your team listed here? Let us Know! Send us a message at: <a href="mailto:info@utahesports.net">info@utahesports.net</a>.</p>
  <hr/>
  <div class="row" style="text-align: center">
    {% for team in site.data.teams-and-clubs %}
      <div class="col-xs-6 col-sm-4" style="margin-top: 50px;">
        <a href="{{ team.url }}">
          <img src="/assets/images/teams/{{ team.image }}.png?" alt="{{ team.name }}"/>
        </a>
        <h3 style="margin-top: 15px;">{{ team.name }}</h3>
        {% if team.level %}
          <div><a href="{{ team.level }}" target="_blank"><i><strong>Level:</strong></i> {{ team.level }}</a></div>
          <hr/>
        {% endif %}
        {% if team.url %}
          <div><a href="{{ team.url }}" target="_blank">Website</a></div>
        {% endif %}
        {% if team.facebook %}
          <div><a href="{{ team.facebook }}" target="_blank">Facebook</a></div>
        {% endif %}
        {% if team.university %}
          <div><a href="{{ team.university }}" target="_blank">University</a></div>
        {% endif %}
        {% if team.twitch %}
          <div><a href="{{ team.twitch }}" target="_blank">Twitch</a></div>
        {% endif %}
        {% if team.twitter %}
          <div><a href="{{ team.twitter }}" target="_blank">Twitter</a></div>
        {% endif %}
        {% if team.instagram %}
          <div><a href="{{ team.instagram }}" target="_blank">Instagram</a></div>
        {% endif %}
        {% if team.discord %}
          <div><a href="{{ team.discord }}" target="_blank">Discord</a></div>
        {% endif %}
        {% if team.youtube %}
          <div><a href="{{ team.youtube }}" target="_blank">Youtube</a></div>
        {% endif %}
        {% if team.steam %}
          <div><a href="{{ team.steam }}" target="_blank">Steam</a></div>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</div>

<style>
  .col-xs-6 a {
    color: #fff;
    font-size: 14px;
    text-decoration: none;
  }
  .col-xs-6 a:hover {
    color: #03A9F3;
  }
  .col-xs-6 img {
    border: 1px solid #2d313a;
  }
</style>