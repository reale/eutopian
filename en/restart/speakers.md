---
layout: page
title: Speakers
lang: en
ref: restart-speakers
permalink: /en/restart/speakers
child_of_ref: restart
order: 5
---

<div class="card-columns">
  {% for speaker in site.data.speakers.speakers %}
  {% assign slug = speaker.name | downcase | replace: ' ', '-' %}
  <div class="card border rounded">
    {% if speaker.headshot != nil and speaker.headshot != "" %}
    <img class="card-img-top" src="/assets/images/headshots/{{ slug }}.{{ speaker.headshot }}" alt="{{ speaker.name }}">
    {% endif %}
    <div class="card-body">
      {% if speaker.bio %}
        <a href="/en/restart/speakers/{{ slug }}" class="card-link"><h5 class="card-title">{{ speaker.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ speaker.name }}</h5>
      {% endif %}

        {% for social-link in speaker.social-links %}
        <!--<li class="list-inline-item">
          <a href="{{ social-link[1] }}" title="{{ social-link[0] }}" target="_blank">
            <svg class="icon"><use xlink:href="{{ site.baseurl }}/assets/bootstrap-italia/dist/svg/sprite.svg#it-{{ social-link[0] }}"></use></svg>
            <span class="sr-only">{{ social-link[0] }}</span>
          </a>
        </li>-->
        <a href="{{ social-link[1] }}" title="{{ social-link[0] }}" target="_blank">{{ social-link[0] }} </a>
        {% endfor %}

    </div>
  </div>
  {% endfor %}
</div>
