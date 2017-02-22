---
layout: post
title: Customize Values| Rating | MobileAspNetMVC | Syncfusion
description: customize values                           
platform: mobileaspnetmvc
control: Rating
keywords: rating
documentation: ug
---

# Customize values                           

The MaximumValue property is used to denote the maximum value up to which the rating can be accepted. The MinimumValue property is used to denote the minimum rating value. The Value property specifies the current selection value. The IncrementStep property specifies the step value incrementation between each rating value (star) selection.

{% highlight html %}

@Html.EJMobile().Rating("rating_sample").MinimumValue(2).MaximumValue(6).Value(4).IncrementStep(1)

{% endhighlight %}

The following screenshot displays the output.

![](Customize-Values_images/Customize-Values_img1.png)



