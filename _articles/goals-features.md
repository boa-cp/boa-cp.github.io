---
layout: post
title:  "Goals and features"
#date:   2020-05-31 22:06:01 +0300
categories: phylosophy
---

Our idea was to create tool for scientists combining havy numbercrunching 
with intuitive interface

### Features:

* Self documnting program
* Program state loging
* Use of all availible computational resorces
* Automatic code documentation readable for non-expirience users
* Work with pysical units

### Self documnting program


### Program state loging

First of all BOA is a python module. Sure it is convinient 
to test directly several commands and to see the result. 
The problem is that in case of success the command hystory 
in not always availible.
We made a try to resolve this problem. Namely, all BOA commands
can be saved: 
{% highlight python %}
boa.saveState("recent-work.py")
{% endhighlight %}

...

