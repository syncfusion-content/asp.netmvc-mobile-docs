---
layout: post
title: Template-Support
description: template support
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

## Template Support

ImageTemplateId and CaptionTemplateId properties are used to customize the image and caption/description of a tile by providing the specific template id respectively. 

Refer to the following code example.

<div style="margin-top:45px;"> 

@Html.EJMobile().Header("head").Title("Tile")

@Html.EJMobile().Tile("tile").ImageTemplateId("imageTemplate").CaptionTemplateId("captionTemplate").TileSize(TileSize.Wide)

<div id="imageTemplate">

   <div id="appimage">

     <div class="tileMargin">

      <span class="caption">Google Search</span><br />

      <span class="description">The world’s information</span><br />

      <span class="sub">Free</span>

     </div>

   </div>

</div>

<div id="captionTemplate" class="title">Windows Store</div>

</div>





The following screenshot illustrates the output of the above code.

{{ '![](Template-Support_images/Template-Support_img1.png)' | markdownify }}
{:.image }


