---
layout: page
permalink: /talks/
title: talks
description: List of presentations I have given
nav: true
---

Je teste..

<!--- {% increment my_row %} --->

<table class="table table-sm">
  {% for row in site.data.presentations %}
    {% if forloop.first %}
    <tr>
      <th>#</th>
      <th>Date</th>
      <th>Type</th>
      <th>Talk title</th>
      <th>Talk context</th>
      <th>Talk location</th>
    </tr>
    {% endif %}

    <tr>
      <td>{% increment my_row %}</td>
      <td>{{ row["event_year"] }}-{{ row["event_month"]}}-{{ row["event_day"]}}</td>
      <td>{{ row["event_type"] }}</td>
      <td>{{ row["event_talk_title"] }}</td>
      <td>{{ row["event_name"] }}</td>
      <td>{{ row["event_location"] }}</td>
    </tr>
  {% endfor %}
</table>
