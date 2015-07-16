---
layout: post
title: Enable-native-scrolling
description: enable native scrolling 
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Enable native scrolling 

Native scrolling refers to the scrolling behavior specific to native devices and it is controlled by the core scrolling engine of native Operating System. By setting the “EnableNativeScrolling” property to true, you can use the default scrolling feature in your device. Disabling this property lets you to use custom scrolling feature. This property is enabled by default for android versions greater than 4.2 and WINRT devices. So, to use Essential MVCScrollPanel, you need to set this property to false.



@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    &lt;div id="maincontent" style="padding:10px"&gt;

        &lt;div&gt;

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        &lt;/div&gt;

    &lt;/div&gt; 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableNativeScrolling(true) 



