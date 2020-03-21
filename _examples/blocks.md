---
layout: post
title:  "Data blocks syntaxis"
#date:   2019-05-09 22:06:01 +0300
categories: examples
---

Here is a simple program demonstrating different syntaxis of Data blocks creation. 

{% highlight python %}
import boa

b1=boa.genBlock(boa.MVec([10]))
print b1
b2=boa.genBlock(boa.MVec([10,3,1]))
print b2
b3=boa.genBlock(boa.MVec([10,3]),boa.MVec([.1,.2]))
print b3
b4=boa.genBlock(boa.MVec([10,3]),boa.MVec([.1,.2]),boa.MVec([100.,.2]))
print b4
b5=boa.genBlock(boa.MVec([10,3]),[.1,.2],[10.,20.])
print b5
{% endhighlight %}

Here is the console output:
{% highlight console %}
Bl{s=10 ; dx=1 ; p=0 }
Bl{s=10 3 1 ; dx=1 1 1 ; p=0 0 0 }
Bl{s=10 3 ; dx=0.1 0.2 ; p=0 0 }
Bl{s=10 3 ; dx=0.1 0.2 ; p=100 0.2 }
Bl{s=10 3 ; dx=0.1 0.2 ; p=10 20 }
{% endhighlight %}
