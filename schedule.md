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
            <p><strong>{{ event.name }}</strong></p>
            <p class="start-time">{{ event.start }}</p>
            <p class="end-time">{{ event.end }}</p>
            <p>{{ event.location }}</p>
          </div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

<script src="../assets/darkmode.js"></script>
<script>
  window.addEventListener("DOMContentLoaded", (event) => {
    onLoad();
    
    // Optional JavaScript logic to handle overlaps dynamically
    const events = document.querySelectorAll('.event');
    events.forEach(event => {
      const startTime = event.querySelector('.start-time').textContent;
      const endTime = event.querySelector('.end-time').textContent;
      
      // You can add your overlap detection logic here and adjust layout accordingly
    });
  });
</script>

<!-- CSS -->
<style>
  .weekly-schedule {
    width: 100%;
  }

  .day-schedule {
    margin-bottom: 20px;
  }

  .events-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .event {
    padding: 10px;
    border-radius: 5px;
    background-color: lightgray;
    width: 48%;
    box-sizing: border-box;
  }

  .red {
    background-color: red;
  }

  .gray {
    background-color: gray;
  }

  @media (max-width: 768px) {
    .event {
      width: 100%;
    }
  }
</style>

