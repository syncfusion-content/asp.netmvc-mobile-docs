---
layout: post
title: dimension
description: dimension
platform: mobileaspnetmvc
control:RadialSlider
documentation: ug
keywords: radialslider , dimension
---

## Dimension

### Stroke width

Radial Slider 'StrokeWidth' property specifies the width of the outline. Refer to the following code example.

{% highlight html %}

               <div class="radialslider default control">
                        <div style="text-align: center">
                            @Html.EJMobile().Button("targetButton").Text("Click here for image zooming").ClientSideEvents(evt => evt.TouchEnd("radialslideropen"))
                        </div>
                    </div>
                    @Html.EJMobile().RadialSlider("defaultradialslider").StrokeWidth(15).AutoOpen(false).Position(RadialSliderPosition.BottomCenter).ClientSideEvents(evt => evt.Change("sliderchange").Slide("sliderchange")).Radius(150).Value(50).Ticks(new List<double>() { 30, 35, 40, 45, 50, 55, 60, 65 })
                    <div id="imagezoom">
                    </div>


{% endhighlight %}

![](dimension_images\stroke-width_img1.png)

