---
layout: base/bar-sidebar-none
title: Calendar

calendar:
  days:
    - date: Tue Mar 29
      location: CSE 403<br>10:00-11:20
      topic: Course Overview and Planning
    - date: Thu Mar 31
      location: CSE 403<br>9:30-11:20
      topic: In-Class Project Discussions
    - date: Tue Apr 5
      location: CSE 403<br>10:00-11:20
      topic: Models of Personal Informatics
      readings: 
        - "Ian Li, Anind Dey, Jodi Forlizzi. (2010).
           [A Stage-Based Model of Personal Informatics Systems](http://dx.doi.org/10.1145/1753326.1753409).
           _CHI 2010_."
        - "Daniel A. Epstein, An Ping, James Fogarty, Sean A. Munson. (2015).
           [A Lived Informatics Model of Personal Informatics](http://dx.doi.org/10.1145/2750858.2804250).
           _UbiComp 2015_."
    - date: Thu Apr 7
      location: CSE 403<br>10:00-11:20
      topic: Project Proposal Presentations
      majors:
        - "Due: [Project Proposal]({{ site.baseurl }}/assignments/project.html#proposal)"
    - date: Tue Apr 12
      location: CSE 403<br>10:00-11:20
      topic: HCI in Promoting Health and Wellness (to be confirmed)
      readings: 
        - "Sunny Consolvo, Predrag Klasnja, David W. McDonald, James A. Landay. (2014). 
           [Designing for Healthy Lifestyles: Design Considerations for Mobile Technologies to Encourage Consumer Health and Wellness](http://dx.doi.org/10.1561/1100000040).
           _Foundations and Trends in Human-Computer Interaction_, 6(3-4), 167-315."
        #
        # Alternative to Consider: 
        # Healthcare in the Pocket: Mapping the Space of Mobile-Phone Health Interventions
        #
    - date: Thu Apr 14
      location: CSE 678<br>9:30-11:20
      topic: Project Advising Meetings
    - date: Tue Apr 19
      location: CSE 403<br>10:00-11:20
      topic: Collection (to be confirmed)
      readings:
        - "Jim Gemmell, Lyndsay Williams, Ken Wood, Roger Lueder, Gordon Bell, Passive Capture and Ensuing Issues for a Personal Lifetime Store, Proceedings of the the 1st ACM workshop on continuous archival and retrieval of personal experiences New York, USA October 2004."
        - QS Paper
      resources:
        - "Felicia Cordeiro, Daniel A. Epstein, Edison Thomaz, Elizabeth Bales, Arvind K. Jagannathan, Gregory D. Abowd, James Fogarty. (2015).
           [Barriers and Negative Nudges: Exploring Challenges in Food Journaling](http://dx.doi.org/10.1145/2702123.2702155).
           _CHI 2015_."
    - date: Thu Apr 21
      location: CSE 678<br>9:30-11:20
      topic: Project Advising Meetings
    - date: Tue Apr 26
      location: CSE 403<br>10:00-11:20
      topic: Integration (to be confirmed)
      readings:
        - haystack
        - Health Mashups
        - "Open mHealth Architecture: An Engine for Health Care Innovation"
    - date: Thu Apr 28
      location: CSE 403<br>10:00-11:20
      topic: Project Progress Presentations
      majors:
        - "Due: [Project Milestone]({{ site.baseurl }}/assignments/project.html#milestone)"
    - date: Tue May 3
      location: CSE 403<br>10:00-11:20
      topic: Reflection (to be confirmed)
      readings: 
        - "reflecting on reflection: Fleck & Fitzpatrick’s paper"
        - cosley pensieve
    - date: Thu May 5
      location: CSE 678<br>9:30-11:20
      topic: Project Advising Meetings
    - date: Tue May 10
      topic: "No Class: CHI 2016 in San Jose, CA"
    - date: Thu May 12
      topic: "No Class: CHI 2016 in San Jose, CA"
    - date: Tue May 17
      topic: "No Class: HDE / QSPH in San Diego, CA"
    - date: Thu May 19
      location: CSE 403<br>10:00-11:20
      topic: Project Progress Presentations
      majors:
        - "Due: [Project Milestone]({{ site.baseurl }}/assignments/project.html#milestone)"
    - date: Tue May 24
      location: CSE 403<br>10:00-11:20
      topic: Action (to be confirmed)
      readings: 
        - "A Taxonomy of Behavior Change Techniques Used in Interventions"
        - "Personalization Revisited: A Reflective Approach Helps People Better Personalize Health Services and Motivates Them to Increase Physical Activity Min Kyung Lee, Junsung Kim, Jodi Forlizzi, Sara Kiesler"
    - date: Thu May 26
      location: CSE 678<br>9:30-11:20
      topic: Project Advising Meetings
    - date: Tue May 31
      location: CSE 403<br>10:00-11:20
      topic: Critical Perspectives (to be confirmed)
      readings: 
        - "Stephen Purpura, Victoria Schwanda, Kaiton Williams, William Stubler, Phoebe Sengers. (2011).
           [Fit4Life: The Design of a Persuasive Technology Promoting Healthy Behavior and Ideal Weight](http://dx.doi.org/10.1145/1978942.1979003).
           _CHI 2011_."
        - "Steps, Choices and Moral Accounting: Observations from a Step-Counting Campaign in the Workplace"
    - date: Thu Jun 2
      location: CSE 678<br>9:30-11:20
      topic: Project Advising Meetings
    - date: Mon Jun 6
      location: CSE 403<br>10:30-12:20
      topic: Final Presentations (to be confirmed)
      majors:
        - "Due: [Final Presentation]({{ site.baseurl }}/assignments/project.html#final-presentation)"
    - date: Tue Jun 7
      topic: Final Report
      majors:
        - "Due: [Final Report]({{ site.baseurl }}/assignments/project.html#final-report)"

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
<ul class="paper" markdown="block">
{% for resource_current in day_current.resources %}
<li class="paper" markdown="block">
{{ resource_current }}
</li>
{% endfor %}
</ul>
{% endif %}

<!----- Majors ----->
{% if day_current.majors %}
{% for major_current in day_current.majors %}
<div class="major" markdown="block">
{{ major_current | liquify }}
</div>
{% endfor %}
{% endif %}

</div>
<!----- End Right Column ----->
</div>
<!----- End Day ----->
{% endfor %}

</div>
</html>
