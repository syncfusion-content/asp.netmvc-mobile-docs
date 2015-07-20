---
layout: post
title: Show-Border
description: show border
platform: mobileaspnetmvc
control: TextArea
documentation: ug
---

## Show Border

ShowBorder property decides whether the Textbox border can be visible or hidden. The default value is true.

Refer to the following code example.

{% highlight html %}



    @Html.EJMobile().TextArea("mailMessage").WatermarkText("TextArea").ShowBorder(false)





{% endhighlight %}



{{ '![](Show-Border_images/Show-Border_img1.png)' | markdownify }}
{:.image }




