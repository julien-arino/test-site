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
      <th>Date</th>
      <th>Type</th>
      <th>Talk title</th>
      <th>Talk context</th>
      <th>Talk location</th>
    </tr>
    {% endif %}

    <td> {{ row["event_year"] }}-{{ row["event_month"]}}-{{ row["event_day"]}} </td>
    <td> {{ row["event_type"] }} </td>
    <td> {{ row["event_talk_title"] }} </td>
    <td> {{ row["event_name"] }} </td>
    <td> {{ row["event_location"] }} </td>
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
