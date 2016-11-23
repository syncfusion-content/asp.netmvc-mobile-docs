---
layout: post
title: Render the specified target| Rotator | MobileAspNetMVC | Syncfusion
description: render the specified target
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Render the specified target

You can render the contents for the Rotator by specifying the particular target element. The target element should maintain the HTML structure as mentioned in the following code example.

The TargetId property is used to define the Id of the target element where you can specify the content to render in the control. The TargetHeight and TargetWidth properties are used to specify the Rotator height and width respectively on initialization. Refer to the following code example.

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

    @{

       @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault");

    }

</div>


{% endhighlight %}


![](Render-the-specified-target_images/Render-the-specified-target_img1.png)



