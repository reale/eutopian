---
layout: page
title: Partners
lang: en
ref: partners
permalink: /en/about-us/partners
child_of_ref: about-us
order: 4
---

<div class="card-columns">
  {% for partner in site.data.partners.partners %}
  <div class="card border rounded">
    {% if partner.logo != nil and partner.logo != "" %}
    <img class="card-img-top" src="/assets/images/logos/{{ partner.ref }}.{{ partner.logo }}" alt="{{ partner.name }}">
    {% endif %}
    <div class="card-body">
      {% if partner.links.website %}
        <a href="{{ partner.links.website }}" class="card-link"><h5 class="card-title">{{ partner.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ partner.name }}</h5>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>
