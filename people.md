---
layout: default
title: People
permalink: /people/
---

<h1>People</h1>

<div class="people-section">
  <h2>Faculty</h2>
  <div class="people-grid" role="list">
    {% for person in site.data.people.faculty %}
      {% include person-card.html person=person %}
    {% endfor %}
  </div>
</div>

<div class="people-section">
  <h2>Affiliated Faculty and Friends</h2>
  <div class="people-grid" role="list">
    {% for person in site.data.people.affiliated %}
      {% include person-card.html person=person %}
    {% endfor %}
  </div>
</div>

<div class="people-section">
  <h2>Students</h2>
  <div class="people-grid" role="list">
    {% for person in site.data.people.students %}
      {% include person-card.html person=person %}
    {% endfor %}
  </div>
</div>

<div class="people-section">
  <h2>Alumni</h2>
  <ul class="people-list">
    {% for person in site.data.people.alumni %}
      {% if person.url %}
        <li><a href="{{ person.url }}">{{ person.name }}</a></li>
      {% else %}
        <li>{{ person.name }}</li>
      {% endif %}
    {% endfor %}
  </ul>
</div>
