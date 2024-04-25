---
title: "Dim Papadopoulos - Publications"
layout: gridlay
excerpt: "Dim Papadopoulos -- Publications."
sitemap: false
permalink: /publications/
---


# Publications


{% for publi in site.data.publist %}

<div class="row">
<div class="col-sm-3">
  <img style="text-align:left;vertical-align: top;margin:0; padding-top:0;" src="{{ site.url }}{{ site.baseurl }}/images/pubpics/{{ publi.image }}" class="img-fluid" width="100%">
</div>
<div class="col-sm-8"> 
  {{ publi.authors }}<br />
  <b>{{ publi.title }}</b> <br />
  <em>{{ publi.conference.full }}</em>, <b>({{ publi.conference.short }})</b>, {{ publi.year }} <br />
  {% if publi.link.website %} <a href="{{ publi.link.website }}"><span class="badge rounded-pill text-bg-dark">PROJECT PAGE</span></a> {% endif %} {% if publi.link.arxiv %} <a href="{{ publi.link.arxiv }}"><span class="badge rounded-pill text-bg-dark">ARXIV</span></a> {% endif %} {% if publi.link.code %} <a href="{{ publi.link.code }}"><span class="badge rounded-pill text-bg-dark">CODE</span></a> {% endif %} {% if publi.link.video  %} <a href="{{ publi.link.video }}"><span class="badge rounded-pill text-bg-dark">VIDEO</span></a> {% endif %}
</div>
</div>

{% endfor %}

