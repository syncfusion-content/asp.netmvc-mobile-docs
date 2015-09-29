---
layout: post
title: Windows Specific Customization| Password | MobileAspNetMVC | Syncfusion
description: windows specific customization
platform: mobileaspnetmvc
control: Password
documentation: ug
---

# Windows Specific Customization

The AllowReset property is used to reset the password value in Windows render mode. The default value is “True”.

Refer to the following code example.

{% highlight html %}



@Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").RenderMode(RenderMode.Windows).Windows(windows=>windows.AllowReset(true))



{% endhighlight %}



![](Windows-Specific-Customization_images/Windows-Specific-Customization_img1.png)



