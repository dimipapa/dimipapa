---
title: "Dim Papadopoulos - Publications"
layout: gridlay
excerpt: "Dim Papadopoulos -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.authors }}<br />
  <b>{{ publi.title }}</b> <br />
  <em>{{ publi.conference.full }}</em>, <b>({{ publi.conference.short }})</b>, {{ publi.year }} <br />
  
  <a href="{{ publi.link.website }}">[Project Page]</a> <a href="{{ publi.link.arxiv }}">[Arxiv]</a> <a href="{{ publi.link.website }}">[Code]</a>

{% endfor %}
