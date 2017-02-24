---
layout: post
title: Select Item| Rotator | MobileAspNetMVC | Syncfusion
description: select item
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Select item

Rotator control takes a numeric value given in CurrentItemIndex property and displays the corresponding item that matches the given index. Refer to the following code example.

{% highlight html %}

<!-- header control -->

@Html.EJMobile().NavigationBar("Header").Mode(NavBarMode.Header).Title("Rotator")



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

    @{         @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").CurrentItemIndex(3);

    }

</div>

{% endhighlight %}



![](Select-Item_images/Select-Item_img1.png)



