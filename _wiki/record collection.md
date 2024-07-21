---
published: true
subtitle:
date: 2024-07-21
tags: 
---

# record collection
{% assign row = site.data.vinylz[0] %} {{ row | inspect }}
{% assign row = site.data.vinylz[0] %}
{% for pair in row %}
  {{ pair | inspect }}
{% endfor %}

<table>
  {% for row in site.data.vinylz %}
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
