---
published: true
subtitle:
date: 2024-07-21
tags: 
---

# record collection
{% assign mydata=site.data.vinylz %}

<table>
    <caption>Table caption</caption>
    <thead>
    {% for column in mydata[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in mydata %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>
