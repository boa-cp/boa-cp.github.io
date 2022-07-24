---
title: Gallery
layout: page
permalink: /Gallery/
---

----

Here yo can find different videos of modeled physical processes. 
All videos are produces by in-house implemented algorithms. 

{% for a in site.gallery %} 
<table>
<tr> <td style="width:20%;"> <a href="{{ a.url | prepend: site.baseurl }}"> <img src="{{a.picture}}" alt="{{a.title}}"> </a> </td>
<td style="width:5%;"></td> 
<td style="width: 259px; vertical-align:top"> <h2> <a href="{{ a.url | prepend: site.baseurl }}">{{a.title}}</a> </h2>
<p> {{a.short}} </p> </td> </tr>
</table>
{% endfor %}

