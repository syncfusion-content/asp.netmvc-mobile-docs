---
layout: post
title: Read Only Support| MaskEdit | MobileAspNetMVC | Syncfusion
description: read only support
platform: mobileaspnetmvc
control: MaskEdit
documentation: ug
---

# Read only support

When it is set to true, you cannot edit the value in the MaskEdit Textbox. The default value is false.

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().MaskEdit("maskedit_sample").WatermarkText("maskedit").Mask("+1 (999) 999-9999").ReadOnly(true)

{% endhighlight %}

![D:/Final Doc/mockup/IMG_0524_iphone5s_spacegrey_portrait.png](Read-Only-Support_images/Read-Only-Support_img1.png)



