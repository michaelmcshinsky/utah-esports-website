---
layout: default
title: All Streams
permalink: /streamers
---

<div style="max-width: 1200px;padding: 0 30px;margin: auto;">
  <div class="heading" style="margin: 50px 0 0">
    <h1>
      Streamers - Full List
    </h1>
  </div>
  <div class="row">
    {% assign sorted_streams = (site.data.streamers | sort: 'streams'') %}
    {% for streamer in sorted_streams %}
    {% assign streams = streamer.streams | split: ' ' %}
    <div class="col-xs-6 col-sm-4 col-md-3">
      <p>{{ streamer.name }}</p>
      <p style="margin-bottom: 0;"><small><strong>Url:</strong> <a href="https://twitch.tv/{{ streamer.name }}" target="_blank">Twitch</a></small></p>
      {% if streamer.youtube %}
        <p><small><strong><a href="{{ streamer.youtube }}" target="_blank">Youtube Channel</a></strong></small></p>
      {% endif %}
      <p><small>
        {% for stream in streams %}
          <a href="/streams/{{ stream }}" style="color: #fff;">{{stream | replace: '-', ' '}}</a><br/>
        {% endfor %}
      </small></p>
    </div>
    {% endfor %}
  </div>
</div>