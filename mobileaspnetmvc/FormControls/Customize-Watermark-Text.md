---
layout: post
title: Customize-Watermark-text
description: customize watermark text
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Customize Watermark text

WatermarkText property is used in customize the text that appears in the background of your Textbox. It acts like a label for the Textbox.

Refer to the following code example.


{% highlight html %}
    @Html.EJMobile().TextBox("textbox_sample").WatermarkText("Textbox")

    @Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password")

    @Html.EJMobile().TextArea("textbox_sample").WatermarkText("Textarea")

    @Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("maskedit").Mask("+1 (999) 999-9999")   
{% endhighlight %}


![C:/Users/isuriyar/AppData/Local/Temp/SNAGHTML8021dede.PNG](Customize-Watermark-text_images/Customize-Watermark-text_img1.png)


