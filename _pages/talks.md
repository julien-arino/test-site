---
layout: page
permalink: /talks/
title: talks
description: List of presentations I have given
nav: true
---

Je teste..


<table>
  {% for row in site.data.presentations %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        {% if pair[0]=="event_type" or pair[0]=="event_year" %}
          <th>{{ pair[0] }}</th>
        {% endif %}
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {% if pair[0]=="event_type" or pair[0]=="event_year" %}
        {{ pair[1] }}
      {% endif %}
    {% endtablerow %}
  {% endfor %}
</table>

<table>
  {% for row in site.data.presentations %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
