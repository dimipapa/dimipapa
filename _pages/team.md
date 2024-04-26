---
title: "Dim Papadopoulos - Team"
layout: gridlay
excerpt: "Dim Papadopoulos: Team members"
sitemap: false
permalink: /team/
---

# Group Members

## Staff
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="35%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <br>email: <{{ member.email }}></i> 
  {% if member.topic  %}
  <ul style="overflow: hidden">
      <li> Co-supervise with {{ member.cosupervisor }} </li>
      <li> Topic: {{ member.topic }} </li>
  </ul>
  {% endif %}
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}



## Master and Bachelor Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Alumni

<div class="row">

<div class="col-sm-12 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
[{{ member.date }}] <b>{{ member.name }}</b>: <i>{{ member.topic }}</i>
{% endfor %}
</div>

<div class="col-sm-12 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{% for member in site.data.alumni_msc %}
[{{ member.date }}] <b>{{ member.name }}</b>: <i>{{ member.topic }}</i>
{% endfor %}
</div>

</div>

