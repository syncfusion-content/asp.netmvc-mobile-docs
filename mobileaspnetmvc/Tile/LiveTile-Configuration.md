---
layout: post
title: LiveTile-Configuration
description: livetile configuration
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

## LiveTile Configuration

Live tiles are used to display the current or up to date information like scores, stocks, weather, etc. This functionality is supported only in windows rendermode. 

You can enable live tile using enabled property (when set to true) that is the sub property of live tile property/object. Type property allows you to specify the type of animation while updating the information in tile. There are three types of tile animation supported, Flip, Slide and Carousel.

ImageUrl property sets background image for live tile. This property accepts array values so you can specify the image url’s for all the tiles that are used in single live tile. 

You can specify time interval for each tile update/animation using UpdateInterval property. Time interval is given in milliseconds. The default value is 2000

Refer to the following code example.



<div style="margin-top:45px;">

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").RenderMode(RenderMode.Windows).LiveTile(live => { live.Enabled(true).Type(LiveTileType.Slide).UpdateInterval(2500).ImageUrl(new string[] { "photo1.png", "photo2.png" }); }).ImagePath(Url.Content("~/themes/sample/tileview")).ImagePosition(TileImagePosition.Fill)

</div>



Using ImageTemplateId property, you can specify live tile images outside the tile rendering. To achieve this, you have to provide image content inside the element where the path is specified by using templateid. You can update the ImageTemplateId dynamically through updateTemplateID public method.

<div style="margin-top:45px;">



@Html.EJMobile().Tile("tile").RenderMode(RenderMode.Windows).LiveTile(live => { live.Enabled(true).ImageTemplateId(new string[] { "temp1", "temp2" }); })

</div>



     <div id="temp1" style="background-image:      

     url('@Url.Content("~/themes/sample/tileview/windows/calendar.png")'); width: 100%; height:    

     100%;">

     </div>

     <div id="temp2" style="background-image:   

     url('@Url.Content("~/themes/sample/tileview/windows/setting.png")'); width: 100%; height:   

     100%;">

     </div>





You can specify the array of images for live tile through CSS classes by using ImageClass property and you can define the desired styles in the specified class.

<div style="margin-top:45px;">



@Html.EJMobile().Tile("tile").RenderMode(RenderMode.Windows).LiveTile(live => { live.Enabled(true).ImageClass(new string[] { "calendar", "setting" }); })

</div>

   <style>

        .calendar {

            background-image: url('../themes/sample/tileview/windows/calendar.png');

        }

        .setting {

            background-image: url('../themes/sample/tileview/windows/setting.png');

        }

    </style>



