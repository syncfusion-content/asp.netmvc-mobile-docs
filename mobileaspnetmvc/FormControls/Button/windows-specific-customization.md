---
layout: post
title: windows-specific-customization
description: windows specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Windows Specific Customization

You can set the **Windows specific** properties to the control by accessing **Windows** property.

**Style**

You can change the style of Windows mode button by accessing **Style** property with **Windows** specific property. 

The possible values are

1. Normal

2. Back

You can refer to the following code examples.



&lt;div align="center" style="margin:10px"&gt;

            @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Windows).Windows(e=>e.Style(WindowsButtonStyle.Normal)) &lt;br /&gt;&lt;br /&gt;



            @Html.EJMobile().ActionLink("sample_button2", "").RenderMode(RenderMode.Windows).Windows(e=>e.Style(WindowsButtonStyle.Back))

&lt;/div&gt;





{% include image.html url="windows-specific-customization_images/windows-specific-customization_img1.png" Caption="Button - Windows Style"%}

