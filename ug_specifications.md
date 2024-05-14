---
layout: default
title: Course Specifications
parent: Undergraduate Program
---

# Undergraduate Course Specifications
{: .no_toc }

1. TOC
{:toc}

## Foundation Courses

{% for course in site.data.courses %}
{% if course.flag == "foundation" %}
### {{ course.course }}: {{ course.title }}
{: .no_toc }

Foundation
{: .label .label-green .float-right}

_({{ course.credits }} credits  / Prerequisites: {{ course.prereqs }})_     
{{ course.description }}
{% if course.specification %}
[Full Course Specification]({{ course.specification }})
{% endif %}

{% endif %}

{% endfor %}


## Elective Courses

{% for course in site.data.courses %}
{% if course.flag == "elective" %}
### {{ course.course }}: {{ course.title }}
{: .no_toc }

Elective
{: .label .label-purple .float-right}

_({{ course.credits }} credits  / Prerequisites: {{ course.prereqs }})_     
{{ course.description }}
{% if course.specification %}
[Full Course Specification]({{ course.specification }})
{% endif %}

{% endif %}

{% endfor %}

## Service Courses

{% for course in site.data.courses %}
{% if course.flag == "service" %}
### {{ course.course }}: {{ course.title }}
{: .no_toc }

Service
{: .label .label-red .float-right}

_({{ course.credits }} credits  / Prerequisites: {{ course.prereqs }})_     
{{ course.description }}
{% if course.specification %}
[Full Course Specification]({{ course.specification }})
{% endif %}

{% endif %}

{% endfor %}