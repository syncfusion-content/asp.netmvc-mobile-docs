---
layout: post
title: Dimensions| Radial Menu | MobileAspNetMVC | Syncfusion
description: dimensions
platform: mobileaspnetmvc
control: Radial Menu
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


@Html.EJMobile().RadialMenu("radialmenu_sample").ImageClass("imageclass").Radius(300).Position(RadialMenuPosition.RightCenter).Items(item =>

{

    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/social.png");

    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/music.png");

    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/direction.png");

    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/message.png");

    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/browser.png");

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
{% highlight javascript %}
<script>

    function click(e) {

        $("#radialmenu_sample").ejmRadialMenu("menuHide");

    }

</script>

{% endhighlight %}
{% endtabs %}


The following screenshot illustrates the output of the above code.

![](Dimensions_images/Dimensions_img1.png)



