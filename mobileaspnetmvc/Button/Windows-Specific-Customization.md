---
layout: post
title: Windows Specific Customization| Button | MobileAspNetMVC | Syncfusion
description: windows specific customization
platform: mobileaspnetmvc
control: Button
documentation: ug
---

# Windows Specific Customization

You can set the **Windows specific** properties to the control by accessing **Windows** property.

## Style

You can change the style of Windows mode button by accessing **Style** property with **Windows** specific property. 

The possible values are

1. Normal

2. Back

You can refer to the following code examples.

{% highlight html %}

<div align="center" style="margin:10px">

@Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Windows).Windows(e=>e.Style(WindowsButtonStyle.Normal)) <br /><br />



@Html.EJMobile().ActionLink("sample_button2", "").RenderMode(RenderMode.Windows).Windows(e=>e.Style(WindowsButtonStyle.Back))

</div>

{% endhighlight %}



{% include image.html url="Windows-Specific-Customization_images/Windows-Specific-Customization_img1.png" Caption="Button - Windows Style"%}

