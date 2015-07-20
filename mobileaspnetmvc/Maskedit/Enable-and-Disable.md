---
layout: post
title: Enable-and-Disable
description: enable and disable
platform: mobileaspnetmvc
control: MaskEdit
documentation: ug
---

## Enable and Disable

Enabled property enables or disables the MaskEditcontrol. The default value is true.

Refer to the following code example.

{% highlight html %}



@Html.EJMobile().MaskEdit("maskedit_sample").WatermarkText("maskedit").Mask("+1 (999) 999-999").Enabled(false)





{% endhighlight %}



{{ '![D:/Final Doc/mockup/IMG_0523_iphone5s_spacegrey_portrait.png](Enable-and-Disable_images/Enable-and-Disable_img1.png)' | markdownify }}
{:.image }


