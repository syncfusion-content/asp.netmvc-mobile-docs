---
layout: post
title: Zooming
description: zooming
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Zooming

EnableZoom is a Boolean property that lets you specify whether the scrolling content can be zoomed or not. By default, this property is set to “false”. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableZoom(true).StartZoom(2).EnableNativeScrolling(false)

{% endhighlight %}

The following screenshot displays zooming:

![](Zooming_images/Zooming_img1.png)



## ZoomMax

ZoomMax property lets you set the maximum limit to which the content can be zoomed. By default, this property is set to 6. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableZoom(true).MaximumZoom(1).StartZoom(2).EnableNativeScrolling(false)

{% endhighlight %}

## ZoomMin

This property lets you set the minimum limit to which the content can be zoomed. By default, this property is set to 1. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableZoom(true).MinimumZoom(2).StartZoom(1).EnableNativeScrolling(false)

{% endhighlight %}

## StartZoom

This property lets you specify the zooming value on initial rendering of the scrollable content.  By default this property is set to 1. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableZoom(true).StartZoom(2).EnableNativeScrolling(false)

{% endhighlight %}

The following screenshot displays the startzoom:

![](Zooming_images/Zooming_img2.png)





