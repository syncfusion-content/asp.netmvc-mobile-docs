---
layout: post
title: Customize-size
description: customize size
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

## Customize size

You can customize the size of tile by using TileSize property. The following built-in tile sizes are supported.

* Medium
* Small
* Large
* Wide



Default value: Small

Refer to the following code example.

&lt;div style="margin-top:45px;"&gt;

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").ImageUrl("map.png").ImagePath(Url.Content("~/themes/sample/tileview")).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("map")

&lt;/div&gt;



The following screenshot illustrates the output of the above code.

{ ![](Customize-size_images/Customize-size_img1.png) | markdownify }
{:.image }


