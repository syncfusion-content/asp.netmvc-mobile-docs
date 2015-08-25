---
layout: post
title: Text-Configuration
description: text configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

# Text Configuration

ShowText property is used to show or hide the tile caption.Text property is used to set the caption of a tile. TextAlignment property is used to align the tile text based on the requirement. The possible position values for TextAlignment are as follows.

1. Normal 
2. Left
3. Right
4. Center

TextPosition property wraps the text inside or outside of a tile. The possible position values of TextPosition are inner and outer.

N> TextPosition support is given only to iOS7 and android mode. Textposition is not supported in small tiles.

{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").ShowText(true).TextAlignment(TextAlignment.Center).Text("Weather").ImageUrl("weather.png").ImagePath("~/themes/sample/tileview").IOS7(item=>item.TextPosition(TileTextPosition.Outer)).ImagePosition(TileImagePosition.Fill)

</div>

{% endhighlight %}

The following screenshot illustrates the output of the above code.

![C:/Users/labuser/AppData/Roaming/Skype/My Skype Received Files/tiletextchanges.png](Text-Configuration_images/Text-Configuration_img1.png)



