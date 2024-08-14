---
layout: home
title: Home
nav_order: 1
nav_exclude: false
permalink: index.html
seo:
  type: Course
  name: Just the Class
---

# Data 6: Introduction to Computational Thinking with Data &#x1f4ca;

{: .mb-2 }
UC Berkeley, Summer 2024
{: .mb-2 .fs-6 .text-grey-dk-000 }

<button class="js-toggle-dark-mode dm-btn btn">Toggle Dark Mode</button>

[Ed](https://edstem.org/us/courses/60192/){: .btn .btn-ed}
[bCourses](https://bcourses.berkeley.edu/courses/1535590){: .btn .btn-bcourses}
[Gradescope](https://www.gradescope.com/courses/800533){: .btn .btn-gradescope}
[Textbook](https://data6.org/su24/resources/#supplemental-readings){: .btn .btn-textbook}
[Jump to Current Week](#week-{{ site.current_week }}){: .btn .btn-currweek}

{: .mb-2 }
**Instructors:**
{: .mb-0 .fs-5 .text-grey-dk-000 }

{% assign instructors = site.staffers | where: 'role', 'InstructorFront' %}

<div class="role flex">
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}
</div>

## Announcements

{% assign announcements = site.announcements | reverse %}
{% for announcement in announcements %}
{{ announcement }}
{% endfor %}


{% assign mods = site.modules | where: 'class', 'Berkeley' %}
{% assign active-mods = '' | split: '' %}

{% for mod in mods %}
  {% if mod.status == 'Active' %}
    {% assign active-mods = active-mods | push: mod %}
  {% endif %}
{% endfor %}

{% for module in active-mods %}
  {{ module }}
{% endfor %}

<!--DARKMODE UNDER CONSTRUCTION-->
<br />

<script src="assets/darkmode.js"></script>
<script>
  const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

  jtd.addEvent(toggleDarkMode, 'click', function(){
    if (jtd.getTheme() === 'custom_dark') {
      jtd.setTheme('light');
      localStorage.setItem("darkMode", 0);
      toggleDarkMode.innerHTML = "Toggle Dark Mode";
      toggleDarkMode.classList.add('dm-btn');
        toggleDarkMode.classList.remove('dm-dark-btn');
    } else {
      jtd.setTheme('custom_dark');
      localStorage.setItem("darkMode", 1);
      toggleDarkMode.innerHTML = "Return to the Light";
      toggleDarkMode.classList.add('dm-dark-btn');
      toggleDarkMode.classList.remove('dm-btn');
    }
  });

    window.addEventListener("DOMContentLoaded", (event) => {
      onLoad();
  });
</script>
