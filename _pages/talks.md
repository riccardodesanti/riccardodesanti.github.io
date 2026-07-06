---
layout: page
permalink: /talks/
title: Talks
description: A chronological list of talks I have given. Slides are linked when available.
nav: true
nav_order: 3
---

<div class="talks talks--full">
{% for talk in site.data.talks_all %}
  <div class="talk">
    <span class="talk-year">
      {%- if talk.date and talk.date != '' -%}
        {%- if talk.date.size == 4 -%}
          {{ talk.date }}
        {%- elsif talk.date.size == 7 -%}
          {{ talk.date | append: '-01' | date: '%b %Y' }}
        {%- else -%}
          {{ talk.date | date: '%b %-d, %Y' }}
        {%- endif -%}
      {%- else -%}
        {{ talk.year }}
      {%- endif -%}
    </span>
    <div class="talk-body">
      {% if talk.slides and talk.slides != '' -%}
        <a class="talk-title" href="{{ talk.slides | relative_url }}">{{ talk.title }}</a>
      {%- else -%}
        <span class="talk-title">{{ talk.title }}</span>
      {%- endif %}
      <div class="talk-venue">
        {%- if talk.venue.url -%}
          <a href="{{ talk.venue.url }}" target="_blank" rel="noopener"><em>{{ talk.venue.name }}</em></a>
        {%- else -%}
          <em>{{ talk.venue.name }}</em>
        {%- endif -%}
        {%- if talk.tag %} <span class="talk-tag">{{ talk.tag }}</span>{% endif -%}
        {%- if talk.note %}, {{ talk.note }}{%- endif -%}
      </div>
    </div>
  </div>
{% endfor %}
</div>
