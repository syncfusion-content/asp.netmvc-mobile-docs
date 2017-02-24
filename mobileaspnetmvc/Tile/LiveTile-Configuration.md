---
layout: post
title: LiveTile Configuration| Tile | MobileAspNetMVC | Syncfusion
description: livetile configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: livetile
---

# LiveTile configuration

Live tiles are used to display the current or up to date information like scores, stocks, weather, etc. This functionality is supported only in windows rendermode. 

You can enable live tile using enabled property (when set to true) that is the sub property of live tile property/object. Type property allows you to specify the type of animation while updating the information in tile. There are three types of tile animation supported, Flip, Slide and Carousel.

ImageUrl property sets background image for live tile. This property accepts array values so you can specify the image url’s for all the tiles that are used in single live tile. 

You can specify time interval for each tile update/animation using UpdateInterval property. Time interval is given in milliseconds. The default value is 2000

Refer to the following code example.

{% highlight html %}

<div style="margin-top:45px;">

@Html.EJMobile().NavigationBar("head").Title("Tileview")

 @Html.EJMobile().Tile("tile").BackgroundColor("#3086e5").RenderMode(RenderMode.Windows).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("People").LiveTile(live => live.Type(LiveTileType.Slide).Enabled(true).UpdateInterval(2500).ImageUrl(new List<string>() {"../themes/sampleimages/tileview/windows/people_1.png" }));

</div>

{% endhighlight %}

Using ImageTemplateId property, you can specify live tile images outside the tile rendering. To achieve this, you have to provide image content inside the element where the path is specified by using templateid. You can update the ImageTemplateId dynamically through updateTemplateID public method.

{% highlight html %}

<div class="tiles" style="top: 45px; position: relative;">
               @Html.EJMobile().Tile("tile").BackgroundColor("#3086e5").RenderMode(RenderMode.Windows).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("People").LiveTile(live => live.ImageTemplateId(new List<string>() { "temp1", "temp2" }).Enabled(true));
    </div>
    <div id="temp1" style="background-image:
            url('../themes/sampleimages/tileview/windows/people_1.png'); width: 100%; height: 100%;">
    </div>
    <div id="temp2" style="background-image:
            url('../themes/sampleimages/tileview/windows/people_3.png'); width: 100%; height: 100%;">
    </div>

{% endhighlight %}

You can specify the array of images for live tile through CSS classes by using ImageClass property and you can define the desired styles in the specified class.

{% tabs %}
{% highlight html %}

<div style="margin-top:45px;">


@Html.EJMobile().Tile("tile").BackgroundColor("#3086e5").RenderMode(RenderMode.Windows).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("People").LiveTile(live => live.ImageClass(new List<string>() { "people_1","people_2" }).Enabled(true));


</div>

{% endhighlight %}


{% highlight css %}

   <style>

       .people_1 {
            background-image: url('../themes/sampleimages/tileview/windows/people_1.png');
        }
        .people_2 {
            background-image: url('../themes/sampleimages/tileview/windows/people_2.png');
        }

    </style>

{% endhighlight %}
{% endtabs %}

You can specify the array of caption text for the Live Tile by Text attribute.

{% highlight html %}

 @Html.EJMobile().Tile("tile").BackgroundColor("#3086e5").RenderMode(RenderMode.Windows).TileSize(TileSize.Medium).ImagePosition(TileImagePosition.Fill).Text("People").LiveTile(live => live.ImageUrl(new List<string>() { "../themes/sampleimages/tileview/windows/people_1.png", "../themes/sampleimages/tileview/windows/people_2.png", "../themes/sampleimages/tileview/windows/people_3.png" }).Enabled(true).Text(new List<string>() {"John","Smith","Johnson" }));

{% endhighlight %}