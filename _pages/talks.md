---
layout: page
permalink: /talks/
title: talks
description: List of presentations I have given
nav: true
---

<!--- {% increment my_row %} --->

<table class="table table-sm">
  <colgroup>
    <col span="1" style="width: 25px;">
    <col span="1" style="width: 80px;">
    <col span="1" style="width: 30px;">
    <col span="1" style="width: 200px;">
    <col span="1" style="width: 150px;">
    <col span="1" style="width: 150px;">
    <col span="1" style="width: 100px;">
  </colgroup>

  {% for row in site.data.presentations %}
    {% if forloop.first %}
    <tr>
      <th>#</th>
      <th>Date</th>
      <th>Type</th>
      <th>Title</th>
      <th>Context</th>
      <th>Location</th>
      <th>Country</th>
    </tr>
    {% endif -%}

    <tr>
      <td>{% increment my_row %}</td>
      {% if row["event_day"].size > 0 -%}
        <td>{{ row["event_year"] }}-{{ row["event_month"]}}-{{ row["event_day"]}}</td>
      {% else -%}
        <td>{{ row["event_year"] }}-{{ row["event_month"]}}</td>
      {% endif -%}
      <td>{{ row["event_type"] }}</td>
      {% if row["event_presentation_file"].size > 0 -%}
        <td><a href="{{ row["event_presentation_file"] -}}">{{ row["event_talk_title"] }}</a></td>
      {% else -%}
        <td>{{ row["event_talk_title"] }}</td>
      {% endif -%}
      {% if row["event_website"].size > 0 -%}
        <td><a href="{{ row["event_website"] -}}">{{ row["event_name"] }}</a></td>
      {% else -%}
        <td>{{ row["event_name"] }}</td>
      {% endif -%}
      <td>{{ row["event_location"] }}</td>
      <td>{{ row["event_country"] }}</td>
    </tr>
  {% endfor -%}

</table>
