---
layout: post
title: Render-the-specified-target
description: render the specified target
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

## Render the specified target

You can render the contents for the Rotator by specifying the particular target element. The target element should maintain the HTML structure as mentioned in the following code example.

The TargetId property is used to define the Id of the target element where you can specify the content to render in the control. The TargetHeight and TargetWidth properties are used to specify the Rotator height and width respectively on initialization. Refer to the following code example.

&lt;!-- header control --&gt;

@Html.EJMobile().Header("header").Title("Photo Gallery")



&lt;div id="rotatorcontentdefault"&gt;

    &lt;div&gt;

        &lt;div class="photo photo1"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo2"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo3"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo4"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo5"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



 &lt;div id="scrollparent"&gt;

    @{

       @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault");

    }

&lt;/div&gt;





{ ![F:/thangavel/dev/source/Trunk/JSDoc/rotator-1.png](Render-the-specified-target_images/Render-the-specified-target_img1.png) | markdownify }
{:.image }


