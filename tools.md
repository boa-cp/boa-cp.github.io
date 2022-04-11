---
title: Tools
layout: page
permalink: /Tools/
---

----
# Calculators

<p>
<table>
{% for a in site.tools %} 
<tr><td><a href="{{ a.url | prepend: site.baseurl }}"> {{a.title}} </a></td></tr>
<tr><td>&nbsp;&nbsp;<small>{{a.categories}} </small></td></tr>
{% endfor %}
</table>
</p>

