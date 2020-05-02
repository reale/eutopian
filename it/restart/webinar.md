---
layout: page
title: Webinar
lang: it
ref: restart-webinar
permalink: /it/restart/webinar
child_of_ref: restart
order: 3
---

<div class="card-columns">
  {% for webinar in site.data.restart.webinars %}
  <div class="card border rounded">
    {% if webinar.image != nil and webinar.image != "" %}
    <img class="card-img-top" src="/assets/images/restart/{{ webinar.ref }}.{{ webinar.image }}" alt="{{ webinar.title }}">
    {% endif %}
    <div class="card-body">
      {% if webinar.permalink %}
        <a href="{{ webinar.permalink }}" class="card-link"><h5 class="card-title">{{ webinar.title }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ webinar.title }}</h5>
      {% endif %}

      {% if webinar.description[page.lang] != nil and webinar.description[page.lang] != "" %}
      <p>{{ webinar.description[page.lang] }}</p>
      {% endif %}

      {% if webinar.speaker != nil and webinar.speaker != "" %}
      {% if webinar.speaker-bio %}
      {% assign speaker-slug = webinar.speaker | downcase | replace: ' ', '-' %}
      <p><b>Keynote speaker:</b> <a href="/it/restart/speaker/{{ speaker-slug }}">{{ webinar.speaker }}</a></p>
      {% else %}
      <p><b>Keynote speaker:</b> {{ webinar.speaker }}</p>
      {% endif %}
      {% endif %}

      {% if webinar.coordinator != nil and webinar.coordinator != "" %}
      {% if webinar.coordinator-bio %}
      {% assign coordinator-slug = webinar.coordinator | downcase | replace: ' ', '-' %}
      <p><b>Coordinamento:</b> <a href="/it/chi-siamo/bio/{{ coordinator-slug }}">{{ webinar.coordinator }}</a></p>
      {% else %}
      <p><b>Coordinamento:</b> {{ webinar.coordinator }}</p>
      {% endif %}
      {% endif %}

      {% if webinar.date != nil and webinar.date != "" %}
      <p>{{ webinar.date }}</p>
      {% endif %}

      {% if webinar.eventbrite != nil and webinar.eventbrite != "" %}
      <p><a href="{{ webinar.eventbrite }}">Iscriviti</a></p>
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
