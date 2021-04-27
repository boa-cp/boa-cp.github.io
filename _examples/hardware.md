---
layout: post
title:  "Computing harware manipulations"
#date:   2019-07-28 22:06:01 +0300
categories: examples
---

Here is a simple program demonstrating different capabilities of the computing hardware monitoring. 

{% highlight python linenos %}
import boa


print "Devices list: ",boa.devicesList()
print "Default device: ", boa.defaultDeviceName()
boa.setDefaultDevice(1)
print "New default device: ",boa.defaultDeviceName()

print "Device 2 name: ",boa.deviceName(2)
print "Device 2 description: "
print boa.deviceDescription(2)

print "Device 3 name: ",boa.deviceName(3)
{% endhighlight %}

Here is the console output:
{% highlight console %}
Devices list:  [(0, 'Intel(R) HD Graphics Skylake Halo GT2'), (1, 'Intel(R) Core(TM) i5-6300HQ CPU @ 2.30GHz'), (2, 'GeForce GTX 960M')]
Default device:  Intel(R) HD Graphics Skylake Halo GT2
New default device:  Intel(R) Core(TM) i5-6300HQ CPU @ 2.30GHz
Device 2 name:  GeForce GTX 960M
Device 2 description: 
NVIDIA Corporation::GeForce GTX 960M
	type: GPU
	number of computer units: 5
	local mem type: LOCAL
	local memory size: 49152
	max item size: 140724741526296
	vector width:
		float: 1
		double: 1
hadware.py:13: RuntimeError: BOA ERROR: There is no device with number: 3
  print "Device 3 name: ",boa.deviceName(3)
Device 3 name: 
Traceback (most recent call last):
  File "hadware.py", line 13, in <module>
    print "Device 3 name: ",boa.deviceName(3)
SystemError: error return without exception set
{% endhighlight %}
