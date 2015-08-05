---
layout: post
title: ios7-specific-customization
description: ios7 specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# IOS7 Specific Customization

You can set the **IOS7 specific** properties to the control by accessing **IOS7** property.

**Color**

This property is specific to **IOS7****RenderMode** that allows you to set the color of the **Button** when used as an action link to indicate the state of the link. 

You can set the text color of the **Button** using ‘**ios7-color’** property.

You can refer to the following code examples.



&lt;div align="center" style="margin:10px"&gt;

@Html.EJMobile().ActionLink("sample_button","").RenderMode(RenderMode.IOS7).IOS7(e=>e.Color(IOS7ButtonColor.Gray)).Text("button") &lt;br /&gt;&lt;br /&gt;

@Html.EJMobile().ActionLink("sample_button","").RenderMode(RenderMode.IOS7).IOS7(e=>e.Color(IOS7ButtonColor.Black)).Text("button") &lt;br /&gt;&lt;br /&gt;

@Html.EJMobile().ActionLink("sample_button","").RenderMode(RenderMode.IOS7).IOS7(e=>e.Color(IOS7ButtonColor.Blue)).Text("button") &lt;br /&gt;&lt;br /&gt;

@Html.EJMobile().ActionLink("sample_button","").RenderMode(RenderMode.IOS7).IOS7(e=>e.Color(IOS7ButtonColor.Green)).Text("button") &lt;br /&gt;&lt;br /&gt;

@Html.EJMobile().ActionLink("sample_button","").RenderMode(RenderMode.IOS7).IOS7(e=>e.Color(IOS7ButtonColor.Red))

&lt;/div&gt;





{% include image.html url="ios7-specific-customization_images/ios7-specific-customization_img1.png" Caption="Button – Ios7-color"%}

**Style**

You can change the style of IOS7 mode button by setting **Style** property with **IOS7** specific property. The possible values are:

1. Normal

2. Back

3. Dialog

4. Header

You can refer to the following code examples.



&lt;div align="center" style="margin:10px"&gt;

                @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.IOS7).IOS7(e => e.Style(IOS7ButtonStyle.Normal)) &lt;br /&gt;&lt;br /&gt;



@Html.EJMobile().ActionLink("sample_button2","").Text("Back").RenderMode(RenderMode.IOS7).IOS7(e => e.Style(IOS7ButtonStyle.Back))



            @Html.EJMobile().Button("sample_button3").Text("Dialog").RenderMode(RenderMode.IOS7).IOS7(e => e.Style(IOS7ButtonStyle.Dialog))



            @Html.EJMobile().Button("sample_button4").Text("Header").RenderMode(RenderMode.IOS7).IOS7(e => e.Style(IOS7ButtonStyle.Header))

    &lt;/div&gt;





{% include image.html url="ios7-specific-customization_images/ios7-specific-customization_img2.png" Caption="Button - IOS7 Style"%}

