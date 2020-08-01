---
layout: page
title: Stakeholders
lang: en
ref: stakeholders
permalink: /en/about-us/stakeholders
child_of_ref: about-us
order: 4
---

<div class="card-columns">
  {% for stakeholder in site.data.stakeholders.stakeholders %}
  <div class="card border rounded">
    {% if stakeholder.logo != nil and stakeholder.logo != "" %}
    <img class="card-img-top" src="/assets/images/logos/{{ stakeholder.ref }}.{{ stakeholder.logo }}" alt="{{ stakeholder.name }}">
    {% endif %}
    <div class="card-body">
      {% if stakeholder.links.website %}
        <a href="{{ stakeholder.links.website }}" class="card-link"><h5 class="card-title">{{ stakeholder.name }}</h5></a>
      {% else %}
        <h5 class="card-title">{{ stakeholder.name }}</h5>
      {% endif %}
      {% if stakeholder.links.document %}
        <a href="{{ stakeholder.links.document }}" class="card-link"><h5 class="card-title">Documents</h5></a>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>
