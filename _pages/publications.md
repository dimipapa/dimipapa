---
title: "Dim Papadopoulos - Publications"
layout: gridlay
excerpt: "Dim Papadopoulos -- Publications."
sitemap: false
permalink: /publications/
---


# Publications


{% for publi in site.data.publist %}

<div class="col-sm-4">
  <img style="text-align:left;vertical-align: top;margin:0; padding-top:0;" src="{{ site.url }}{{ site.baseurl }}/images/pubpics/{{ publi.image }}" width="100%">
</div>
<div class="col-sm-8"> 
  {{ publi.authors }}<br />
  <b>{{ publi.title }}</b> <br />
  <em>{{ publi.conference.full }}</em>, <b>({{ publi.conference.short }})</b>, {{ publi.year }} <br />
  <a href="{{ publi.link.website }}">[Project Page]</a> <a href="{{ publi.link.arxiv }}">[Arxiv]</a> <a href="{{ publi.link.website }}">[Code]</a>
</div>

{% endfor %}
