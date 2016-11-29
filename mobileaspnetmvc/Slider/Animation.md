---
layout: post
title: Animation| Slider | MobileAspNetMVC | Syncfusion
description: animation
platform: mobileaspnetmvc
control: Slider
keywords: slider, animation
documentation: ug
---

# Animation

EnableAnimation property is used to enable or disable the Animation effect in the Slider. Default value for this property is set to “false”.  AnimationSpeed property specifies the animation speed when the Slider is dragged from long range. It works only when “EnableAnimation” property is set to true. Default Value is “400”.

{% highlight html %}

@Html.EJMobile().Slider("slider_sample").EnableAnimation(true).AnimationSpeed(1000)


{% endhighlight %}
