---
layout: page
title: Home
---
THIS IS A test for the home page!

special symbol indicates it is a mouse that hasn't been released yet.
 - create feature to e-mail user when mouse is released, and provide them a link to it. No account needed. just email address.

Here is the table:


<table>
  {% for row in site.data.raw-mouse-data %}
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


<script src="https://www.kryogenix.org/code/browser/sorttable/sorttable.js"></script>
<script>
    var table = document.querySelector("table");
    sorttable.makeSortable(table);
</script>