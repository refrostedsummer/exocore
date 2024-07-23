---
published: true
datatable: true
subtitle:
date: 2024-07-21
tags: 
---

# music ratings


<table>
  {% for row in site.data.vinylz}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endfor %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>