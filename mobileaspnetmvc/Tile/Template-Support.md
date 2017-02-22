---
layout: post
title: Template Support| Tile | MobileAspNetMVC | Syncfusion
description: template support
platform: mobileaspnetmvc
control: Tile
documentation: ug
keywords: template
---

# Template support

ImageTemplateId and CaptionTemplateId properties are used to customize the image and caption/description of a tile by providing the specific template id respectively. 

Refer to the following code example.

{% highlight html %}

<div style="margin-top:45px;"> 

@Html.EJMobile().NavigationBar("head").Title("Tile")

  @Html.EJMobile().Tile("tileview1").BackgroundColor("#3086e5").Caption(c => c.Alignment(TextAlignment.Center).Text("Weather")).TileSize(TileSize.Wide).ImageTemplateId("imageTemplate")

</div>
    <div id="imageTemplate">
        <div id="appimage">
        </div>
        <div class="tileMargin">
            <span class="caption">Google Search</span><br />
            <span class="description">The world’s information</span><br />
            <span class="sub">Free</span>
        </div>
    </div>
{% endhighlight %}
Refer the below code snippets for CSS classes

{% highlight html %}
 #appimage {
            background-image: url("../themes/sampleimages/rating/google.png");
            background-repeat: no-repeat;
            width: 70px;
            height: 70px;
            background-size: 100%;
            float: left;
        }

        #imageTemplate {
            margin-top: 35px;
            margin-left: 10px;
        }

        .tileMargin {
            padding-left: 77px;
            color: white;
        }
{% endhighlight %}
The following screenshot illustrates the output of the above code.

![](Template-Support_images/Template-Support_img1.png)



