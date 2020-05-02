---
layout: page
title: Speaker
lang: it
ref: restart-speakers
permalink: /it/restart/speaker
child_of_ref: restart
order: 5
---

<div class="card-columns">
  {% for member in site.data.speakers.speakers %}
  {% assign slug = member.name | downcase | replace: ' ', '-' %}
  <div class="card border rounded">
    {% if member.headshot != nil and member.headshot != "" %}
    <img class="card-img-top" src="/assets/images/headshots/{{ slug }}.{{ member.headshot }}" alt="{{ member.name }}">
    {% endif %}
    <div class="card-body">
      {% if member.bio %}
        <a href="/it/restart/speaker/{{ slug }}" class="card-link"><h5 class="card-title">{{ member.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ member.name }}</h5>
      {% endif %}

        {% for social-link in member.social-links %}
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
