---
layout: post
title: Customize value| Slider | MobileAspNetMVC | Syncfusion
description: customize value
platform: mobileaspnetmvc
control: Slider
keywords: slider, value
documentation: ug
---

# Customize value

Value property is used to set the value for the Slider on initialization. MaximumValue sets the maximum value the Slider can hold and MinimumValue sets the minimum value the Slider can hold. IncrementStep property specifies the step-by-step increment value of the Slider when the Slider knob is dragged. You can refer the following code example.

{% highlight html %}

@Html.EJMobile().Slider("slider_sample").Value(80).MinimumValue(10).MaximumValue(100).IncrementStep(10)

{% endhighlight %}

The following screenshot displays the customized Slider Value:

![](Customize-value_images/Customize-value_img1.png)



