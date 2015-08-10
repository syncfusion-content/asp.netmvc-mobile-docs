---
layout: post
title: windows-specific-customization
description: windows specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Windows specific customization

The **AllowReset** property is used to reset the password value in windows rendermode. The default value is **true.**

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").RenderMode(RenderMode.Windows).Windows(windows=>windows.AllowReset(true))

{% endhighlight %}

{% include image.html url="windows-specific-customization_images/windows-specific-customization_img1.png" Caption="Textbox - AllowReset"%}

