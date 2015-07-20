---
layout: post
title: Flat-Specific-Customization
description: flat specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Flat Specific Customization

You can set the Flat mode specific properties to the control by accessing Flat property.

Styles

You can change the style of Flat mode button by accessing Style property with Flat specific property. 

The possible values are

1. Normal
2. Back
3. Header

You can refer to the following code examples.



<div align="center" style="margin:10px">

            @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Normal)) <br /><br />



@Html.EJMobile().ActionLink("sample_button1", "").Text("Back").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Back)) <br /><br />

      @Html.EJMobile().Button("sample_button1").Text("Header").RenderMode(RenderMode.Flat).Flat(e => e.Style(FlatButtonStyle.Header))

</div>





{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML2ab540a8.PNG](Flat-Specific-Customization_images/Flat-Specific-Customization_img1.png)' | markdownify }}
{:.image }


