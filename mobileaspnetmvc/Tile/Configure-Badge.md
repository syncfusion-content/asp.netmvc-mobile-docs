---
layout: post
title: Configure Badge| Tile | MobileAspNetMVC | Syncfusion
description: configure badge
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: badge
---

# Configure badge

The Badge property handles badge specific functionalities like enable or disable the badge and setting badge value for tile. The Text property is used to set the text instead of number for tile badge. The MaxValue and MinValue properties areusedto set the maximum and minimum badge value to a tile respectively. 

Refer to the following code example.

{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().NavigationBar("head").Title("Tile")

 @Html.EJMobile().Tile("tile").ImageUrl("messaging.png").ImagePath(Url.Content("http://js.syncfusion.com/UG/Mobile/Content/tile")).Text("Messaging").Badge(badge => { badge.Enabled(true).MaxValue(80).MinValue(10).Value(88); })

</div>

{% endhighlight %}

The following screenshot illustrates the output of the above code.

![](badge-configuration_images/badge-configuration_img1.png)



