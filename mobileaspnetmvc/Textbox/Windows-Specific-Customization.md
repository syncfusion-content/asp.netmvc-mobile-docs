---
layout: post
title: Windows Specific Customization| Textbox | MobileAspNetMVC | Syncfusion
description: windows specific customization
platform: mobileaspnetmvc
control: Textbox
documentation: ug
---

# Windows specific customization

The **AllowReset** property is used to reset the password value in windows rendermode. The default value is **true.**

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").RenderMode(RenderMode.Windows).Windows(windows=>windows.AllowReset(true))

{% endhighlight %}

{% include image.html url="Windows-Specific-Customization_images/Windows-Specific-Customization_img1.png" Caption="Textbox - AllowReset"%}

