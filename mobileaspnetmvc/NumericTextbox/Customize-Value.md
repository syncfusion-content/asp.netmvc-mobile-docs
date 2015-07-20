---
layout: post
title: Customize-Value
description: customize value
platform: mobileaspnetmvc
control: Numeric Textbox
documentation: ug
---

## Customize Value

The current value of the Numeric Textbox can be specified by using the Value property. The range for the Numeric Textbox can be specified by using the MaxValue and MinValue properties. The Numeric Textbox can only accept values within the specified range. The IncrementStep property is used to set the step value in each incrementing or decrementing textbox when the spin buttons are clicked or when the up or down arrows are used.

{% highlight html %}

@Html.EJMobile().NumericTextbox("textbox_sample").Value("30").IncrementStep(2).MaximumValue(100).MinimumValue(3)





{% endhighlight %}

The following screenshot displays the output.

{{ '![http://help.syncfusion.com/ug/js/ImagesExt/image20_41.png](Customize-Value_images/Customize-Value_img1.png)' | markdownify }}
{:.image }


{% highlight html %}

@Html.EJMobile().NumericTextbox("textbox_sample").DecimalPlaces(3)



{% endhighlight %}



