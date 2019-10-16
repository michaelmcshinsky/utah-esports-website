---
layout: default
title: Social Groups
header:
  teaser: "/assets/images/site/logo-square.png"
permalink: /social-groups
---

<div style="max-width: 1200px;margin: 50px auto;padding: 0 30px;">
  <div class="heading" style="margin: 50px 0 0">
    <h1>
      {{ page.title }}
    </h1>
  </div>
  <p>There is no better way to game than knowing there are a community of active local gamers who have your back! We love supporting the community so much that we have created a mini directory of all the gaming communities online located here in Utah. Utah Esports hopes you find the resources and friends here to make your gaming experience beyond fun!</p>
  <p>Are we missing any information? If so, let us know at <a href="mailto:info@utahesports.net">info@utahesports.net</a>.</p>
  <hr/>
  <div class="row">
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Super Smash Brothers</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "super-smash-brothers" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">League of Legends</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "league-of-legends" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Starcraft</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "starcraft" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Halo</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "halo" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Dota 2</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "dota" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Hearthstone</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "hearthstone" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Heroes of the Storm</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "heroes-of-the-storm" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Call of Duty</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "call-of-duty" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Battlefield</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "battlefield" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Overwatch</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "overwatch" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Counterstrike</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "counterstrike" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Warcraft</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "warcraft" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Fortnite</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "fortnite" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <div class="col-xs-6 col-sm-4">
      <h3 style="margin-top: 50px;font-size: 20px;">Misc</h3>
      <br/>
      {% for group in site.data.social-groups %}
        {% if group.tag == "misc" %}
          <div>
            <a href="{{ group.url }}" target="_blank">{{ group.name }}</a>
          </div>
        {% endif %}
      {% endfor %}
    </div>
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