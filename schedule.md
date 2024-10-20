---
layout: page
title: Schedule
description: The weekly event schedule.
---

# Weekly Schedule

{% for schedule in site.schedules %}
{{ schedule }}
{% endfor %}

<script src="../assets/darkmode.js"></script>
<script>
  window.addEventListener("DOMContentLoaded", (event) => {
    onLoad();
});
</script>
