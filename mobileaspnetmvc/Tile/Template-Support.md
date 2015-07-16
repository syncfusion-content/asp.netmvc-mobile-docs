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

&lt;div style="margin-top:45px;"&gt; 

@Html.EJMobile().Header("head").Title("Tile")

@Html.EJMobile().Tile("tile").ImageTemplateId("imageTemplate").CaptionTemplateId("captionTemplate").TileSize(TileSize.Wide)

&lt;div id="imageTemplate"&gt;

   &lt;div id="appimage"&gt;

     &lt;div class="tileMargin"&gt;

      <span class="caption">Google Search</span>&lt;br /&gt;

      <span class="description">The world’s information</span>&lt;br /&gt;

      <span class="sub">Free</span>

     &lt;/div&gt;

   &lt;/div&gt;

&lt;/div&gt;

<div id="captionTemplate" class="title">Windows Store</div>

&lt;/div&gt;





The following screenshot illustrates the output of the above code.

{ ![](Template-Support_images/Template-Support_img1.png) | markdownify }
{:.image }


