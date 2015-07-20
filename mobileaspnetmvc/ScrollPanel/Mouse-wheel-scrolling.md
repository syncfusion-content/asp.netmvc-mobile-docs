---
layout: post
title: Mouse-wheel-scrolling
description: mouse wheel scrolling
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Mouse wheel scrolling

The “EnableMouseWheel” is a Boolean property that lets you decide whether or not the ScrollPanel can be controlled by using mouse wheel. By default, this property is set to true.

You can adjust the scrolling speed with respect to Mouse wheel speed. This can be achieved by using “WheelSpeed” property. By default, this property is set to 16.



@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").WheelSpeed(20).EnableNativeScrolling(false).EnableMouseWheel(true)



