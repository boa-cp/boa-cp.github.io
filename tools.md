---
title: Tools
layout: page
permalink: /Tools/
---

----
# Calculators

{% for a in site.tools %} | [{{ a.title }}]({{ a.url | prepend: site.baseurl }})  | {{a.categories}} |
{% endfor %}

