---
layout: post
title: Image Configuration| Tile | MobileAspNetMVC | Syncfusion
description: image configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: tile , image 
---

# Image configuration

"ImagePosition" property is used to adjust the position of tile image. It accepts the following values.

1. Center
2. TopCenter
3. BottomCenter
4. RightCenter
5. LeftCenter
6. TopLeft
7. BottomRight
8. BottomLeft 
9. Fill
10.TopRight



BackgroundColor property is used to set the background color of the tile.

ImageUrl property is used to specify the file name for the background image of tile. The imagepath property is used to define the root path that should contain the following folder structure to automatically render the background image based on the device/platform it gets rendered. All these three folder should contain the image files (with same name, but different images) that can be specified in image url property.

* iOS7 - Folder name for ios7 specific images
* Android - Folder name for Android specific images
* Windows - Folder name for Windows specific images



Note: Both ImagePath and ImageUrl properties can be set when you want to specify separate images for each render mode and so it is necessary to specify separate path for iOS, android and windows rendermode. When ImageUrl property is alone used, you can provide common images for all render modes. you can provide common images for all render modes. So, you should provide the whole image path for this attribute.



{% highlight html %}

<div style="margin-top:45px;">
    @Html.EJMobile().NavigationBar("head").Title("Tile")

    <div style="margin-top:45px;">

        @Html.EJMobile().Tile("tile").ImagePosition(TileImagePosition.Fill).ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").ImageUrl("setting.png").Caption(c => c.Alignment(TextAlignment.Left).Text("Settings")).TileSize(TileSize.Small).ShowRoundedCorner(true).ImagePosition(TileImagePosition.Fill)
    </div>

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](Image-Configuration_images/Image-Configuration_img1.png)



Also you can give images for each Tile through CSS classes by using the ImageClass attribute. You can define your desired styles in the specified class.

Refer to the following code example.

{% tabs %}
{% highlight html %}
        @Html.EJMobile().NavigationBar("head").Title("Tile")
    <div style="margin-top:45px;">

        @Html.EJMobile().Tile("tile").ImageClass("picture").Text("Music").ShowRoundedCorner(true)

    </div>

</div>

{% endhighlight %}

{% highlight css %}

<style>

.picture {
            background-image: url("http://js.syncfusion.com/UG/Mobile/Content/tile/music.png");
         }

    </style>

{% endhighlight %}
{% endtabs %}

The following screenshot illustrates the output of the above code.

![](Image-Configuration_images/Image-Configuration_img2.png)



