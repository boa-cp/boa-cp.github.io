---
title: Articles
layout: page
permalink: /articles/
---

{% for a in site.articles %}
[{{ a.title }}]({{ a.url | prepend: site.baseurl }})
{% endfor %}

