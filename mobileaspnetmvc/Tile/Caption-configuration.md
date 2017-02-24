---
layout: post
title: Text Configuration| Tile | MobileAspNetMVC | Syncfusion
description: text configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: tile , caption
---

# Caption configuration

The `data-ej-caption-enabled` attribute is used to show or hide the **Tile caption**. The `data-ej-caption-text` attribute is used to set the caption of a Tile. The `data-ej-caption-alignment` attribute is used to align the Tile text based on the requirement. The possible position values for `alignment` are as follows.

1. normal

2. left

3. right

4. center

The `data-ej-caption-position` attribute wraps the text inside or outside of a Tile. The possible position values of `data-ej-caption-position` are innertop, innerbottom and outer.

N> Caption position is not supported in small Tiles except ios and android outer position.



{% highlight html %}


    <div class="tiles" style="top: 45px; position: relative;">
           @Html.EJMobile().Tile("tileview1").ShowRoundedCorner(true).ImagePosition(TileImagePosition.Fill).Caption(c => c.Alignment(TextAlignment.Center).Text("Weather")).TileSize(TileSize.Small).ImageUrl("http://js.syncfusion.com/UG/Mobile/Content/tile/weather.png")
    </div>


{% endhighlight %}



The following screenshot illustrates the output of the above code.

![](caption-configuration_images\caption-configuration_img1.png)

