---
layout: post
title: customize-value
description: customize value
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Customize value

The current value of the **Numeric Textbox** can be specified by using **Value** property. The range for the **Numeric Textbox** can be specified by using the **MaxValue** and **MinValue** properties. The **Numeric Textbox** can only accept values within those specified range. The **IncrementStep** property is used to set the step value in each incrementing or decrementing textbox when the spin buttons are clicked or up/down arrows are used.



@Html.EJMobile().NumericTextbox("textbox_sample").**Value("30")**.**IncrementStep(2)**.**MaximumValue(100)**.**MinimumValue(3)**



The following screenshot displays the output.

{% include image.html url="customize-value_images/customize-value_img1.png" Caption="Numeric Textbox-Value"%}



@Html.EJMobile().NumericTextbox("textbox_sample").**DecimalPlaces(3)**



