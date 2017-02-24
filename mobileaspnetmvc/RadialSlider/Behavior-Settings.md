---
layout: post
title: behavior-settings
description: behavior settings
platform: mobileaspnetmvc
control: RadialSlider
documentation: ug
keywords: radialslider, position
---

# Behavior settings

The following are some properties that enables you to an option to enhance the behavior of RadialSlider control.

## Show/hide RadialSlider on initial rendering

The RadialSlider  "AutoOpen" property allow you to make the control visible on initial rendering. By default, the value of the property is set as true. Setting it as false will hide the control on initial rendering.

{% highlight html %}

   @Html.EJMobile().RadialSlider("defaultradialslider").AutoOpen(true).Position(RadialSliderPosition.BottomCenter).ClientSideEvents(evt => evt.Change("sliderchange").Slide("sliderchange")).Radius(150).Value(50).Ticks(new List<double>() { 30, 35, 40, 45, 50, 55, 60, 65 })


{% endhighlight %}

![](behavior-settings_images\showhide-radialslider-on-initial-rendering_img1.png)

## Position

The RadialSlider property position allows you to make the position of the control.

{% highlight html %}

   
@Html.EJMobile().RadialSlider("defaultradialslider").AutoOpen(true).Position(RadialSliderPosition.LeftCenter).ClientSideEvents(evt => evt.Change("sliderchange").Slide("sliderchange")).Radius(150).Value(50).Ticks(new List<double>() { 30, 35, 40, 45, 50, 55, 60, 65 })


{% endhighlight %}

![](behavior-settings_images\position_img1.png)


## RoundOff

The RadialSlider property EnableRoundOff allows you to make the position of the control.

{% highlight html %}

   @Html.EJMobile().RadialSlider("defaultradialslider").AutoOpen(true).Position(RadialSliderPosition.LeftCenter).EnableRoundOff(false).ClientSideEvents(evt => evt.Change("sliderchange").Slide("sliderchange")).Radius(150).Value(50).Ticks(new List<double>() { 30, 35, 40, 45, 50, 55, 60, 65 })

{% endhighlight %}



![](behavior-settings_images\roundoff_img1.png)

