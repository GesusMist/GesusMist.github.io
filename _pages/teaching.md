---
layout: page
permalink: /teaching/
title: teaching
description: Materials for courses you taught.
nav: true
nav_order: 6
courses:
  - code: SI100B
    title: Introduction to Information Science and Technology
    term: Spring 2025
    role: Teaching Assistant
    institution: ShanghaiTech University
  - code: CS100
    title: 	Introduction to	Programming
    term: Spring 2024
    role: Teaching Assistant
    institution: ShanghaiTech University

# Add one item per course you TA'd under `courses:`.
# Example:
# courses:
#   - code: CSCE 000
#     title: Course Title
#     term: Fall 2025
#     role: Teaching Assistant
#     institution: Texas A&M University
---

{% if page.courses and page.courses.size > 0 %}
<ul>
  {% for course in page.courses %}
    <li>
      {% if course.code and course.title %}
        <strong>{{ course.code }}</strong>: {{ course.title }}
      {% elsif course.title %}
        <strong>{{ course.title }}</strong>
      {% elsif course.code %}
        <strong>{{ course.code }}</strong>
      {% endif %}
      {% if course.term %}, {{ course.term }}{% endif %}
      {% if course.role %} ({{ course.role }}){% endif %}
      {% if course.institution %}, {{ course.institution }}{% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
Add your TA courses to the `courses` list in this file.
{% endif %}
