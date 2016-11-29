---
layout: post
title: Dimensions| Radial Menu | MobileAspNetMVC | Syncfusion
description: dimensions
platform: mobileaspnetmvc
control: Radial Menu
keywords: radialmenu, dimensions
documentation: ug
---

# Dimensions

You can customize Radial Menu width (radius) by using Radius property and its position by using Position property.

The Possible values for Position property are

* Leftcenter
* Lefttop
* Leftbottom
* Rightcenter   
* Righttop
* Rightbottom

{% tabs %}
{% highlight html %}


        @Html.EJMobile().RadialMenu("defaultradialmenu").Position(RadialMenuPosition.RightCenter).Radius(100).ImageClass("imageclass").Items(item =>
{
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/music.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/social.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/direction.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/browser.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/message.png");
})

{% endhighlight  %}
{% highlight css %}
<style>

 .imageclass {
        background: url("http://js.syncfusion.com/UG/Mobile/Content/radial/radialSettings.png");
        background-position: center;
        background-repeat: no-repeat;
    }

</style>
{% endhighlight %}

{% endtabs %}


The following screenshot illustrates the output of the above code.

![](Dimensions_images/Dimensions_img1.png)



