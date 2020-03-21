---
layout: post
title:  "Work with writers and messages"
#date:   2019-05-09 22:06:01 +0300
categories: examples
---

Here is a simple program demonstrating use of build in "Messanging system". 

{% highlight python %}
import boa

boa.writeMessage("Message 1")
boa.writeWarning("Warning 1")
boa.writeError("Error 1")
boa.writeMessage("Message 1a")

boa.mwInit_File("message1.txt")
boa.writeMessage("Message 2")

boa.mwInit_FileTerminal("message2.txt")
boa.writeMessage("Message 3")

boa.ewInit_FileTerminal("error.txt")
boa.writeError("Error 2")
{% endhighlight %}

Here is the console output:
{% highlight console %}
Message 1
WARNING: Warning 1
writing.py:4: RuntimeError: BOA ERROR: Error 1
  boa.writeError("Error 1")
Message 1a
XX message2.txt
Message 3
writing.py:14: RuntimeError: BOA ERROR: Error 2
  boa.writeError("Error 2")
{% endhighlight %}

message1.txt:
{% highlight console %}
Message 2
{% endhighlight %}
message2.txt
{% highlight console %}
Message 3
{% endhighlight %}
error.txt
{% highlight console %}
BOA ERROR: Error 2
{% endhighlight %}


