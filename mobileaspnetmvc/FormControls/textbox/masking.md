---
layout: post
title: masking
description: masking
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Masking

It can be done using **Mask Edit****Textbox** control. When you define an input mask using the **Mask** property, each character position in the **Mask Edit** control maps to either a placeholder of a specified type or a literal character.

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("Maskedit").Mask("+1 (999) 999-999")  

{% endhighlight %}



{% include image.html url="masking_images/masking_img1.png" Caption="Textbox –mask property"%}

