---
layout: post
title: Select-Item
description: select item
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

## Select Item

Rotator control takes a numeric value given in CurrentItemIndex property and displays the corresponding item that matches the given index. Refer to the following code example.

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

    @{         @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").CurrentItemIndex(3);

    }

&lt;/div&gt;





{ ![F:/thangavel/dev/source/Trunk/JSDoc/rotator-2.png](Select-Item_images/Select-Item_img1.png) | markdownify }
{:.image }


