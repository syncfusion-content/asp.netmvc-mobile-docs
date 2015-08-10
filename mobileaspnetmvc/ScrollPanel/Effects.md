---
layout: post
title: Effects
description: effects
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

# Effects

## Bouncing

You can add bouncing effect to your application to indicate that you have reached the end of page while scrolling. The “EnableBounce” property allows you to enable or disable the bouncing effect by setting the values to true or false respectively. By default, this property is set to true.

The “BounceTime” property specifies the reset timing of the content when it scrolls beyond the limit of x and y positions with respect to the wrapper element. By default, this property is set to 450.

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> @Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableNativeScrolling(false).EnableBounce(true) .BounceTime(200)
	
{% endhighlight %}

## Fading

The “EnableFade” is a Boolean property used to enable or disable the fade of scrollbars at the end of Scrolling. By default, this property is set to true. Refer to the following code example.

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> @Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableFade(false).EnableNativeScrolling(false)

		
{% endhighlight %}

## Shrinking

The “EnableShrink” is a Boolean property that lets you to specify whether the scrollbars can be shrunk or not (when it reaches the top or bottom of the page).

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableShrink(true).EnableNativeScrolling(false)

{% endhighlight %}

## Transform and Transitions

The “EnableTransform” property lets you specify whether to use transform method (animation) for scrolling or not. The “EnableTransition” property lets you specify whether to use transition method (animation) for scrolling or not. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableNativeScrolling(false).EnableTransform(true).EnableTransition(true)


{% endhighlight %}
