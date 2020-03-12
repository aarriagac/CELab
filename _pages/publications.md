---
title: "CELab - Publicaciones"
layout: gridlay
excerpt: "CELab -- Publicaciones."
sitemap: false
permalink: /publicaciones/
---


# Publicaciones

---
Puede ver la lista completa en la siguiente
<a class="liga" href="#lista-completa">sección</a>
o puede revisar <a class="liga" href="https://scholar.google.com/citations?user=4zBCxAgAAAAJ&hl=es&oi=sra">Google Scholar</a>.

## Destacadas

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="row">
 	<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="25%" style="float: right" />
  <p><a class="pub3">{{ publi.title }}</a></p>
  <p><em>{{ publi.authors }}</em></p>
  <a class="pub2" href="{{ publi.link.url }}"> {{ publi.link.display }} </a>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

---

<div>

## Lista Completa

{% for publi in site.data.publist %}

  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }} </em><br /><a class="liga" href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

<!-- For a full list, please go to <a class="regtext" href="https://scholar.google.com/citations?user=O1EuSPYAAAAJ">Google Scholar</a> or <a class="regtext" href="https://www.ncbi.nlm.nih.gov/pubmed?term=Sanders%20SJ%5BAuthor%5D">Pubmed</a>.
<br><br><br>
-->
</div>
