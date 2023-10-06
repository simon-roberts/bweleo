---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

## Management

{% assign instructors = site.staffers | where: 'role', 'Management' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Volunteer' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Volunteers

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
