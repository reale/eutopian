---
layout: page
title: Our team
lang: en
ref: team
permalink: /en/about-us/team
child_of_ref: about-us
order: 2
---

## Founders

<div class="card-columns">
  {% for member in site.data.members.founders %}
  {% assign slug = member.name | downcase | replace: ' ', '-' %}
  <div class="card border rounded">
    {% if member.headshot != nil and member.headshot != "" %}
    <img class="card-img-top" src="/assets/images/headshots/{{ slug }}.{{ member.headshot }}" alt="{{ member.name }}">
    {% endif %}
    <div class="card-body">
      {% if member.bio %}
        <a href="/en/about-us/bio/{{ slug }}" class="card-link"><h5 class="card-title">{{ member.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ member.name }}</h5>
      {% endif %}

      {% if member.role != nil and member.role != "" %}
      <p>{{ member.role[page.lang] }}</p>
      {% endif %}

      <div class="it-socials">
        <ul class="px-0">
        {% for social-link in member.social-links %}
        <li class="list-inline-item">
          {% if social-link[0] == "mail" %}{% assign schema = "mailto:" %}{% else %}{% assign schema = "" %}{% endif %}
          <a href="{{ schema }}{{ social-link[1] }}" title="{{ social-link[0] }}" target="_blank">
            <svg class="icon icon-primary"><use xlink:href="{{ site.baseurl }}/assets/bootstrap-italia/dist/svg/sprite.svg#it-{{ social-link[0] }}"></use></svg>
            <!--<span class="sr-only">{{ social-link[0] }}</span>-->
          </a>
        </li>
        {% endfor %}
        </ul>
      </div>

    </div>
  </div>
  {% endfor %}
</div>

## Ordinary Members

<div class="card-columns">
  {% for member in site.data.members.ordinary %}
  {% assign slug = member.name | downcase | replace: ' ', '-' %}
  <div class="card border rounded">
    {% if member.headshot != nil and member.headshot != "" %}
    <img class="card-img-top" src="/assets/images/headshots/{{ slug }}.{{ member.headshot }}" alt="{{ member.name }}">
    {% endif %}
    <div class="card-body">
      {% if member.bio %}
        <a href="/en/about-us/bio/{{ slug }}" class="card-link"><h5 class="card-title">{{ member.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ member.name }}</h5>
      {% endif %}

      {% if member.role != nil and member.role != "" %}
      <p>{{ member.role[page.lang] }}</p>
      {% endif %}

      <div class="it-socials">
        <ul class="px-0">
        {% for social-link in member.social-links %}
        <li class="list-inline-item">
          {% if social-link[0] == "mail" %}{% assign schema = "mailto:" %}{% else %}{% assign schema = "" %}{% endif %}
          <a href="{{ schema }}{{ social-link[1] }}" title="{{ social-link[0] }}" target="_blank">
            <svg class="icon icon-primary"><use xlink:href="{{ site.baseurl }}/assets/bootstrap-italia/dist/svg/sprite.svg#it-{{ social-link[0] }}"></use></svg>
            <!--<span class="sr-only">{{ social-link[0] }}</span>-->
          </a>
        </li>
        {% endfor %}
        </ul>
      </div>

    </div>
  </div>
  {% endfor %}
</div>
