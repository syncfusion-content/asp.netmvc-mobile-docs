---
layout: post
title: Native TimePicker| TimePicker | MobileAspNetMVC | Syncfusion
description: native timepicker
platform: mobileaspnetmvc
control: TimePicker
documentation: ug
---

# Native TimePicker

The RenderDefault property is used to enable iOS7 native TimePicker instead of the Syncfusion’sTimePicker; but by using iOS7 native TimePicker, you cannot customize theme, etc. The default value is false.

{% highlight html %}

@Html.EJMobile().TimePicker("timepicker").RenderMode(RenderMode.IOS7).IOS7(IOS7 => IOS7.RenderDefault(true)).HourFormat(HourFormat.Twelve)

{% endhighlight %}

The following screenshot displays the output.

![](Native-TimePicker_images/Native-TimePicker_img1.png)



