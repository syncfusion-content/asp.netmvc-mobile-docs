---
layout: post
title: Get Mobile Grid object| Grid | MobileAspNetMVC | Syncfusion
description: get mobile grid object	
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Get Mobile Grid object	

After you initialize Mobile Grid, Grid object is stored in container element of Grid. To access Mobile Grid object refer the following code sample.

{% highlight javascript %}

var gridObject = $("#MobileGrid").ejmGrid("instance");



                [or]




var gridObject = $("#MobileGrid ").data("ejmGrid");


{% endhighlight %}






