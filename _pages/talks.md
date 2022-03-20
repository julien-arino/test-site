---
layout: page
permalink: /talks/
title: talks
description: A list of presentations
nav: true
---

Je teste..

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
