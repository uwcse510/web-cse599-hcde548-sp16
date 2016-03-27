---
layout: base/bar-sidebar-none
title: Calendar

calendar:
  days:
    - date: Tue Mar 29
      topic: Course Overview and Planning
      location: CSE 403
    - date: Thu Mar 31
      topic: TBD
    - date: Tue Apr 5
      topic: Models of Personal Informatics
      location: CSE 403
      readings: 
        - Ian Li, Anind Dey, Jodi Forlizzi. 
          [A Stage-Based Model of Personal Informatics Systems](http://dx.doi.org/10.1145/1753326.1753409).
          _CHI 2010_.
        - Daniel A. Epstein, An Ping, James Fogarty, Sean A. Munson. 
          [A Lived Informatics Model of Personal Informatics](http://dx.doi.org/10.1145/2750858.2804250).
          _UbiComp 2015_.
    - date: Thu Apr 7
      topic: TBD
    - date: Tue Apr 12
      topic: TBD
      location: CSE 403
    - date: Thu Apr 14
      topic: Project Advising Meetings
    - date: Tue Apr 19
      topic: TBD
      location: CSE 403
    - date: Thu Apr 21
      topic: Project Advising Meetings
    - date: Tue Apr 26
      topic: TBD
      location: CSE 403
    - date: Thu Apr 28
      topic: Project Advising Meetings
    - date: Tue May 3
      topic: TBD
      location: CSE 403
    - date: Thu May 5
      topic: Project Advising Meetings
    - date: Tue May 10
      topic: "No Class: CHI 2016 in San Jose, CA"
    - date: Thu May 12
      topic: "No Class: CHI 2016 in San Jose, CA"
    - date: Tue May 17
      topic: "No Class: HDE / QSPH in San Diego, CA"
    - date: Thu May 19
      topic: Project Advising Meetings
    - date: Tue May 24
      topic: TBD
      location: CSE 403
    - date: Thu May 26
      topic: Project Advising Meetings
    - date: Tue May 31
      topic: TBD
      location: CSE 403
---

` This page is under development and everything is subject to change `

<html>
<div class="calendar">

{% for day_current in page.calendar.days %}
<!----- Day ----->
<div class="row">
<!----- Left Column ----->
<div class="col-md-2" markdown="block">
## {{ day_current.date }}

<div class="directions" markdown="block">
{% if day_current.location %}
{{ day_current.location }}
{% endif %}
</div>

</div>
<!----- End Left Column ----->
<!----- Right Column ----->
<div class="col-md-10 calcontent" markdown="block">
## {{ day_current.topic }}

<!----- Readings ----->
{% if day_current.readings %}
<div class="directions" markdown="block">
Readings Assigned:
</div>
<ul class="paper" markdown="block">
{% for reading_current in day_current.readings %}
<li class="paper" markdown="block">
{{ reading_current }}
</li>
{% endfor %}
</ul>
{% endif %}

<!----- Resources ----->
{% if day_current.resources %}
<div class="directions" markdown="block">
Additional Resources:
</div>
{% endif %}

</div>
<!----- End Right Column ----->
</div>
<!----- End Day ----->
{% endfor %}

</div>
</html>
