---
layout: page
title: Schedule
description: The weekly event schedule.
---

# Weekly Schedule

<div class="weekly-schedule">
  {% for day in site.schedules %}
    <div class="day-schedule">
      <h2>{{ day.name }}</h2>
      <div class="events-container">
        {% for event in day.events %}
          <div class="event {{ event.style | default: 'default-style' }}">
            <strong>{{ event.name }}</strong><br>
            <span>{{ event.start }} - {{ event.end }}</span><br>
            <span>{{ event.location }}</span>
          </div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

<script src="../assets/darkmode.js"></script>
