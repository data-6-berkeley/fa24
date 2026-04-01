---
layout: page
title: Schedule
description: The weekly event schedule.
---

{: .warning }
⚠️ This content is archived as of March 2026 and is retained exclusively for reference. [Find current offerings.](https://data6.org/)

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
