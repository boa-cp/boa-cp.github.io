---
layout: post
title:  "Work with parameters"
#date:   2019-05-09 22:06:01 +0300
categories: examples
---

Here is a simple program demonstrating use of build in "Parameters Management" capabilities. 

{% highlight python %}

import boa
boa.pmInit_INIFile("test.ini")
a=boa.genFParameter("a",2.2,"test parameter F")
b=boa.genIParameter("b",3,"test parameter I")
c=boa.genIParameter("a.b",3,"test parameter G")
print "a=",a," #", a.description()
print "b=",b," #", b.description()
print "c=",c," #", c.description()

print "Let's read the \"test.ini\" file..."
boa.pmUpdate()

print "a=",a," #", a.description()
print "b=",b," #", b.description()
print "c=",c," #", c.description()

{% endhighlight %}

Here the corresponding "test.ini" content:
{% highlight ini %}
a=3.5
[a]
b=10
{% endhighlight %}


Here is the console output:
{% highlight console %}
a=  2.2  # test parameter F
b=  3  # test parameter I
c=  3  # test parameter I
Let's read the "test.ini" file...
a=  3.5  # test parameter F
b=  3  # test parameter I
c=  10  # test parameter I
{% endhighlight %}

It is seen that the parameters have the default values initially. The command
{% highlight python %}
boa.pmUpdate()
{% endhighlight %}
causes to read the parameters from the .ini file. Note, the syntax of the "c" variable in the .ini file. It is useful if you have sectioning the input file.

