---
layout: post
title: Controlling-through-keys
description: controlling through keys
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Controlling through keys

The “EnableKeys” property lets you decide whether the scrollpanel can be controlled by using Arrow keys or not. 



@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    &lt;div id="maincontent" style="padding:10px"&gt;

        &lt;div&gt;

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        &lt;/div&gt;

    &lt;/div&gt; 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableKeys(false).EnableNativeScrolling(false)



