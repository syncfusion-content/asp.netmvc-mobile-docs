---
layout: post
title: Image Configuration| Tile | MobileAspNetMVC | Syncfusion
description: image configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

# Image Configuration

ImagePosition property is used to adjust the position of tile image. It accepts the following values.

1. Center
2. Top
3. Bottom
4. Right
5. Left
6. TopLeft
7. BottomRight
8. BottomLeft 
9. Fill



BackgroundColor property is used to set the background color of the tile.

ImageUrl property is used to specify the file name for the background image of tile. The imagepath property is used to define the root path that should contain the following folder structure to automatically render the background image based on the device/platform it gets rendered. All these three folder should contain the image files (with same name, but different images) that can be specified in image url property.

* iOS7 - Folder name for ios7 specific images
* Android - Folder name for Android specific images
* Windows - Folder name for Windows specific images



Note: Both Imagepath and imageurl properties can be set when you want to specify separate images for each render mode and so it is necessary to specify separate path for iOS, android and windows rendermode. When Imageurl property is alone used, you can provide common images for all render modes. That is you should provide the whole image path for this property.



{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").ImagePosition(TileImagePosition.Fill).ImagePath("~/themes/sample/tileview").ImageUrl("Weather_1.png").BackgroundColor("#ae12ae").Text("Weather")</div>


{% endhighlight %}


The following screenshot illustrates the output of the above code.

![C:/Users/labuser/AppData/Roaming/Skype/My Skype Received Files/imagepositionchange.png](Image-Configuration_images/Image-Configuration_img1.png)



Also you can give images for each tile through CSS classes by using ImageClass property. You can define your desired styles in the specified class.

Refer to the following code example.

{% tabs %}
{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").ImageClass("picture").Text("Weather")

</div>

{% endhighlight %}

{% highlight css %}

<style>

.picture {

background-image: url("../themes/sample/tileview/windows/calculator.png");

background-color: #ae12ae;

background-size: 40px 40px;

}

    </style>

{% endhighlight %}
{% endtabs %}

The following screenshot illustrates the output of the above code.

![C:/Users/labuser/Desktop/ImagClass.png](Image-Configuration_images/Image-Configuration_img2.png)



