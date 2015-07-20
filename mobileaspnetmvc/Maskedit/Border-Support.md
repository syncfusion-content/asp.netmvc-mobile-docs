---
layout: post
title: Border-Support
description: border support
platform: mobileaspnetmvc
control: MaskEdit
documentation: ug
---

## Border Support

ShowBorder property is used to decide whether the MaskEdit Textbox border can be visible or hidden. The default value is true.

Refer to the following code example.

{% highlight html %}



@Html.EJMobile().MaskEdit("maskedit_sample").WatermarkText("Maskedit").ShowBorder(false).Mask("+1 (999) 999-999")  





{% endhighlight %}



{{ '![D:/Final Doc/mockup/IMG_0522_iphone5s_spacegrey_portrait.png](Border-Support_images/Border-Support_img1.png)' | markdownify }}
{:.image }


