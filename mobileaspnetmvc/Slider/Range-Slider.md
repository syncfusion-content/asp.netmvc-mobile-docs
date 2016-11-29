---
layout: post
title: Range Slider| Slider | MobileAspNetMVC | Syncfusion
description: range slider
platform: mobileaspnetmvc
control: Slider
keywords: slider, rangeslider
documentation: ug
---

# Range Slider

The “EnableRange” property is used to select the range of values that is from and to values. The “Values” property specifies the “from” and “to” values for the RangeSlider on initialization. Default value of the “EnableRange” property is set to “false”.

{% highlight html %}

    @Html.EJMobile().Slider("slider_sample").EnableRange(true).Values(new int[] {30, 90})

{% endhighlight %}

The following screenshot displays the Range of the Slider:

![](Range-Slider_images/Range-Slider_img1.png)



