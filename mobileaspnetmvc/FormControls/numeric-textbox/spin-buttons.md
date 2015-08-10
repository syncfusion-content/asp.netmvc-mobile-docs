---
layout: post
title: spin-buttons
description: spin buttons
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Spin buttons

ShowSpinButton property is used to specify whether the Spin Button is visible or hidden. By clicking these buttons, you can increment or decrement the Numeric value.

{% highlight html %}

@Html.EJMobile().NumericTextbox("textbox_sample").ShowSpinButton(false)

{% endhighlight %}

The following screenshot displays the output.

{% include image.html url="spin-buttons_images/spin-buttons_img1.png" Caption="Numeric Textbox - Show Spin Button"%}

