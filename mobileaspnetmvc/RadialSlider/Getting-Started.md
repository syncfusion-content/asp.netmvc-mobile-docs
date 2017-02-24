---
layout: post
title: getting-started
description: getting started
platform: mobileaspnetmvc
control: RadialSlider
documentation: ug
keywords: radialslider
---

# Getting started

This section explains briefly on how to create a Radial Slider control in your mobile application.

![](getting-started_images\getting-started_img1.png)

## Create basic mobile layout

In the following section, you can learn to create a basic mobile layout using RadialSlider control.

Create a simple MVC application and paste the following header in layout page content inside the <body>tag of layout.cshtml.You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started).

{% highlight html %}
       <!-- header control -->

        @Html.EJMobile().NavigationBar("header").Title("RadialSlider")

        <div id="accordion" class="sample">

            <div>

                <!--Render Radial Slider control-->

            </div>

        </div>

       
{% endhighlight %}

## Add Radial Slider control

Add the below code to render the Radial Slider

{% highlight html %}

                    <!-- Render Menu control -->
                    <div class="radialslider default control">
                        <div style="text-align: center">
                            @Html.EJMobile().Button("targetButton").Text("Click here for image zooming").ClientSideEvents(evt => evt.TouchEnd("radialslideropen"))
                        </div>
                    </div>
                    @Html.EJMobile().RadialSlider("defaultradialslider").AutoOpen(false).Position(RadialSliderPosition.BottomCenter).ClientSideEvents(evt => evt.Change("sliderchange").Slide("sliderchange")).Radius(150).Value(50).Ticks(new List<double>() { 30, 35, 40, 45, 50, 55, 60, 65 })
                    <div id="imagezoom">
                    </div>

{% endhighlight %}



{% highlight js %}

function RadialSliderLoad() {
            if ($("#appList").is(":visible"))
                $("#defaultradialslider").css("left", parseInt($("#defaultradialslider").css("left")) - 140)
        }
        function radialslideropen(args) {

            $("#defaultradialslider").ejmRadialSlider("show");
        }
        function sliderchange(args) {
            $("#imagezoom").css("background-size", args.value + "%")
        }
        function RadialSliderRenderModeLoad() {
            $("#defaultradialslider").ejmRadialSlider({ value: 50, ticks: [30, 35, 40, 45, 50, 55, 60, 65] });
            $("#imagezoom").css("background-size", "50%")
        }


{% endhighlight %}

![](getting-started_images\add-radial-slider-control_img1.png)

