---
layout: post
title: IOS7 Specific Customization| Slider | MobileAspNetMVC | Syncfusion
description: ios7 specific customization
platform: mobileaspnetmvc
control: Slider
keywords: slider, ios
documentation: ug
---

# IOS7 Specific Customization

You can set the IOS7 specific properties to the control by accessing IOS7 property.

## ThumbStyle

ThumbStyle property is used to render the Slider knob in two different styles.  Default value for the property is set to “Normal”.

The possible values are,

1. Normal
2. Small

{% highlight html %}

@Html.EJMobile().Slider("slider_sample").RenderMode(RenderMode.IOS7).IOS7(ios => ios.ThumbStyle(ThumbStyle.Small))

{% endhighlight %}

The following screenshot displays the Slider iOS7:

![](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img1.png)



## Orientation

It specifies the Orientation in which the Slider is rendered. By default, the value is set to “horizontal”.

The possible values are,

1. Horizontal
2. Vertical

{% highlight html %}

@Html.EJMobile().Slider("slider_sample").Orientation(Orientation.Vertical)

{% endhighlight %}

The following screenshot displays the Slider Orientation:

![](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img2.png)



## Readonly

ReadOnly property makes the Slider control to be fixed. When this property is set to true, the Slider knob cannot be dragged from its current position that is the Slider value cannot be changed.

{% highlight html %}

@Html.EJMobile().Slider("slider_sample").ReadOnly(true)

{% endhighlight %}

