{% extends "section.md" %}

{% block body %}

{% for school in items %}
  <strong> {{school.school}} </strong>, {{school.location}}<br>
  {% if school.department %}
    <i>{{school.department}}</i>,
  {% endif %}
  {{school.degree}}, {{school.completion}}

<!-- <table class="table table-hover"> -->
<!--   <tr>
    <td class="col-md-3">{{ school.dates }}</td>
    <td>
      {% if school.degree %}
        <strong>{{ school.degree }}</strong>
        {% if school.overallGPA %}
          ({{ school.overallGPA }})
        {% endif %}
        <br>
      {% endif %}
      {{ school.school }}
    </td>
  </tr> -->
{% endfor %}
</table>
{% endblock body %}
