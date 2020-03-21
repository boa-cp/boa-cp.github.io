---
layout: page
title: Examples
permalink: /examples/
---

{% for a in site.examples %}
[{{ a.title }}]({{ a.url | prepend: site.baseurl }})
{% endfor %}

