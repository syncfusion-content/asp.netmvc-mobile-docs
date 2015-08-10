---
layout: post
title: show-border
description: show border
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Show Border

**ShowBorder** property is used to decide whether the **Textbox** border can be visible or hidden. The default value is true.

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().TextBox("textbox_sample").WatermarkText("Textbox").ShowBorder(false)



    @Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").ShowBorder(false)



    @Html.EJMobile().TextArea("textbox_sample").WatermarkText("Textarea").ShowBorder(false)



    @Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("Maskedit").ShowBorder(false).Mask("+1 (999) 999-999")  

{% endhighlight %}

{% include image.html url="show-border_images/show-border_img1.png" Caption="Figure 33: Textbox -Show Border"%}

