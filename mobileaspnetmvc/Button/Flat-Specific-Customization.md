---
layout: post
title: Flat Specific Customization| Button | MobileAspNetMVC | Syncfusion
description: flat specific customization
platform: mobileaspnetmvc
control: Button
documentation: ug
---

# Flat Specific Customization

You can set the **Flat mode specific** properties to the control by accessing **Flat** property.

## Styles

You can change the style of Flat mode button by accessing **Style** property with **Flat** specific property. 

The possible values are

1. Normal

2. Back

3. Header

You can refer to the following code examples.

{% highlight html %}

<div align="center" style="margin:10px">

            @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Normal)) 



@Html.EJMobile().ActionLink("sample_button1", "").Text("Back").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Back))

      @Html.EJMobile().Button("sample_button1").Text("Header").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Header))

<div>


{% endhighlight %}


{% include image.html url="Flat-Specific-Customization_images/Flat-Specific-Customization_img1.png" Caption="Button - Flat Style"%}

