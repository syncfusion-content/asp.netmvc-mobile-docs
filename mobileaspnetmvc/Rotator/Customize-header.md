---
layout: post
title: Customize header| Rotator | MobileAspNetMVC | Syncfusion
description: customize header
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Customize header

In Rotator you can enable the built-in header support. You can use Title property. You can set the title for NavigationBar using Title property. Refer to the following code example.

{% highlight html %}

<!-- header control -->

@Html.EJMobile().NavigationBar("Header").Mode(NavBarMode.Header).Title("Photo Gallery")



<div id="rotatorcontentdefault">

    <div>

        <div class="photo photo1">

        </div>

    </div>

    <div>

        <div class="photo photo2">

        </div>

    </div>

    <div>

        <div class="photo photo3">

        </div>

    </div>

    <div>

        <div class="photo photo4">

        </div>

    </div>

    <div>

        <div class="photo photo5">

        </div>

    </div>

</div>



<div id="scrollparent">

    @{    @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault");

    }

</div>

{% endhighlight %}



![](Customize-header_images/Customize-header_img1.png)



