---
layout: post
title: Strict-Mode-Support
description: strict mode support
platform: mobileaspnetmvc
control: Numeric Textbox
documentation: ug
---

## Strict Mode Support

The EnableStrictMode property makes Textbox accept only a value between the defined maximum and minimum values when it is set to “True”.

{% highlight html %}

@Html.EJMobile().NumericTextbox("textbox_sample").MinimumValue(30).MaximumValue(100)


.EnableStrictMode(true)


{% endhighlight %}

The following screenshot displays the output.

![][http://help.syncfusion.com/ug/js/ImagesExt/image20_42.png](Strict-Mode-Support_images/Strict-Mode-Support_img1.png)


