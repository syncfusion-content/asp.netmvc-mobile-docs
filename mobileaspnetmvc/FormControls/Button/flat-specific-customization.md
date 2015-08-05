---
layout: post
title: flat-specific-customization
description: flat specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Flat Specific Customization

You can set the **Flat mode specific** properties to the control by accessing **Flat** property.

**Styles**

You can change the style of Flat mode button by accessing **Style** property with **Flat** specific property. 

The possible values are

1. Normal

2. Back

3. Header

You can refer to the following code examples.



&lt;div align="center" style="margin:10px"&gt;

            @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Normal)) &lt;br /&gt;&lt;br /&gt;



@Html.EJMobile().ActionLink("sample_button1", "").Text("Back").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Back)) &lt;br /&gt;&lt;br /&gt;

      @Html.EJMobile().Button("sample_button1").Text("Header").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Header))

&lt;/div&gt;





{% include image.html url="flat-specific-customization_images/flat-specific-customization_img1.png" Caption="Button - Flat Style"%}

