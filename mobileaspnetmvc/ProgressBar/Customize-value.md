---
layout: post
title: Customize value| ProgressBar | MobileAspNetMVC | Syncfusion
description: customize value
platform: mobileaspnetmvc
control: ProgressBar
keywords: progressbar, value
documentation: ug
---

# Customize value

The current value of the ProgressBar is specified by using 'Value' property. "MaxValue" property holds the maximum value where the progress ends. MinValue property holds the minimum value where the progress starts. Set the step value to be added in each increment when progress goes on by using the IncrementStep property. You can refer to the following code examples.

{% highlight html %}

@Html.EJMobile().ProgressBar("progressbar_sample").Value(55).MaximumValue(90).MinimumValue(10).IncrementStep(5)

{% endhighlight %}

Output of customize value:

![](Customize-value_images/Customize-value_img1.png)



