---
layout: page
title: Webinars
lang: en
ref: restart-webinar
permalink: /en/restart/webinars
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
      <p><b>Keynote speaker:</b> {{ webinar.speaker }}</p>
      {% endif %}

      {% if webinar.coordinator != nil and webinar.coordinator != "" %}
      <p><b>Coordinator:</b> {{ webinar.coordinator }}</p>
      {% endif %}

      {% if webinar.date != nil and webinar.date != "" %}
      <p>{{ webinar.date }}</p>
      {% endif %}

      {% if webinar.eventbrite != nil and webinar.eventbrite != "" %}
      <p><a href="{{ webinar.eventbrite }}">Register</a></p>
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
