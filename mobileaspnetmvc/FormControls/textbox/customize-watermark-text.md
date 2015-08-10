---
layout: post
title: customize-watermark-text
description: customize watermark text
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Customize Watermark text

**WatermarkText** property is used in customize the text that appears in the background of your **Textbox**. It acts like a label for the **Textbox**.

Refer to the following code example.
{% highlight html %}


    @Html.EJMobile().TextBox("textbox_sample").WatermarkText("Textbox")

    @Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password")

    @Html.EJMobile().TextArea("textbox_sample").WatermarkText("Textarea")

    @Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("maskedit")**.Mask("+1 (999) 999-9999")   

{% endhighlight %}

{% include image.html url="customize-watermark-text_images/customize-watermark-text_img1.png" Caption="Textbox - Water Mark Text"%}

