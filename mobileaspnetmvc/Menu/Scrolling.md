---
layout: post
title: Scrolling| Menu | MobileAspNetMVC | Syncfusion
description: scrolling 	
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Scrolling 	

The AllowScrolling property defines whether to allow the scrolling behavior or not when the number of Menu items exceed the specified Menu height.The default value of allowscrolling  property  is true.
{% highlight html %}

	<div style="text-align: center;">

	@Html.EJMobile().Button("menuitem").Text("Menu")

	</div>
@Html.EJMobile().Menu("menu_sample").Target("menuitem").Height("200").Items(item =>
    {

        item.Add().Text("Get info");

        item.Add().Text("Show in folder");

        item.Add().Text("Delete");

        item.Add().Text("Get info");

        item.Add().Text("Show in folder");

        item.Add().Text("Delete");

        item.Add().Text("Get info");

        item.Add().Text("Show in folder");

        item.Add().Text("Delete");

    })


{% endhighlight %}

The following screenshot displays Scrolling:

![](Scrolling_images/Scrolling_img1.png)



