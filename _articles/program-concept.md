---
layout: post
title:  "Typical program structure"
#date:   2019-05-09 22:06:01 +0300
categories: phylosophy
---

### Overview

The typical program structure is as follows:

* Program parameters definition and reading
* Data blocks
* Geometry definition objects
* Data fields with initialization
* Numerical method and boundary conditions
* Iteration loop
* Data output

### Libtrary loading

{% highlight python %}
import boa
{% endhighlight %}

### Parameters definition 

{% highlight python %}
boa.addParameterD("g","gravity acceleration in m/s^2", 0.5)
boa.addParameterD("object1.l","object1 length, m", 1)
{% endhighlight %}

The corresponding ini file can looks as follows: 
{% highlight ini %}
g = 0.5 #gravity acceleration in m/s^2
[object1]
l = 1
{% endhighlight %}

### Data blocks

to be continued ...

