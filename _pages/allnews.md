---
title: "CELab - Noticias"
layout: textlay
excerpt: "CELab at UASLP."
sitemap: false
permalink: /noticias/
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
