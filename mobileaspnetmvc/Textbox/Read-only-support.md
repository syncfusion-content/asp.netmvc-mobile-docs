---
layout: post
title: Read only support| Textbox | MobileAspNetMVC | Syncfusion
description: read only support
platform: mobileaspnetmvc
control: Textbox
keywords: textbox, readonly
documentation: ug
---

# Read only support

When ReadOnly property is set to true, you cannot edit the value in the Textbox. The default value is false.

Refer to the following code example.

{% highlight html %}



@Html.EJMobile().TextBox("textbox_sample").WatermarkText("Textbox").ReadOnly(true)



{% endhighlight %}



The following screenshot displays the ReadOnly property set to true.

![](Read-only-support_images/Read-only-support_img1.png)



