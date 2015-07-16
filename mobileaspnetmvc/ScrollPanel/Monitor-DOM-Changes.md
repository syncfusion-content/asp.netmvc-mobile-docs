---
layout: post
title: Monitor-DOM-Changes
description: monitor dom changes
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Monitor DOM Changes

The “CheckDOMChanges” property lets you specify whether or not to refresh the Scrollpanel automatically when elements are added to the DOM tree dynamically. By default, this property is set to false. 

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    &lt;div id="maincontent" style="padding:10px"&gt;

        &lt;div&gt;

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.

        &lt;br /&gt;                          @Html.EJMobile().Button("sample_button").Text("click_me").ClientSideEvents(e => e.TouchStart("touchstart"))

&lt;/div&gt;

    &lt;/div&gt;

  @Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").CheckDOMChanges(true).EnableNativeScrolling(false)



    &lt;script&gt;

        function touchstart() {

                 $("#content").append("Dynamically added content<br/>") ;  }

    &lt;/script&gt;





