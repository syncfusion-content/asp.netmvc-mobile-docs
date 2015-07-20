---
layout: post
title: Android-specific-customization
description: android specific customization
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Android specific customization

You can set the Android Specific properties to the control by accessing Android property.

BackButtonImageClass

This feature specifies the class name in which an image for the back button is set.  Refer to the following code example.

@Html.EJMobile().Header("header_sample").RenderMode(RenderMode.Android).ShowLeftButton(true).Android(p=>{p.BackButtonImageClass("img");})

    <style>

        .img {

            background: url("pin.png") no-repeat;

        }

    </style> 

The following screenshot displays the Android Specific customization:

{{ '![F:/android_phone.png](Android-specific-customization_images/Android-specific-customization_img1.png)' | markdownify }}
{:.image }


