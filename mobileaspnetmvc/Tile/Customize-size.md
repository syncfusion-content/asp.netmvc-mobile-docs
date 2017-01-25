---
layout: post
title: Customize size| Tile | MobileAspNetMVC | Syncfusion
description: customize size
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: size
---

# Customize size

You can customize the size of tile by using TileSize property. The following built-in tile sizes are supported.

* Medium
* Small
* Large
* Wide



Default value: Small

Refer to the following code example.

{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().NavigationBar("head").Title("Tileview")

 @Html.EJMobile().Tile("tile").ImageUrl("map.png").ImagePath(Url.Content("http://js.syncfusion.com/UG/Mobile/Content/tile")).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("map")

</div>

{% endhighlight %}

The following screenshot illustrates the output of the above code.

![](Customize-size_images/Customize-size_img1.png)



