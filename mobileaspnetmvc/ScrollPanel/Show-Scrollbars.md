---
layout: post
title: Show-Scrollbars
description: show scrollbars
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

# Show Scrollbars

The “ShowScrollbars” property is to control the visibility of the Scrollbars in your application. By default, this property is set to true. 

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("ScrollPanel")

    <div id="maincontent" style="padding:10px">

        <div>

            Founded by industry experts in 2001, Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform. With Syncfusion, developers can move beyond simply coding applications to delivering real business innovation—the elegant user interfaces, business intelligence dashboards, and sophisticated reporting that today's business users need, in the formats they demand. Our award-winning .NET components and controls are designed to meet your evolving development needs, whether you're working in Windows Forms, WPF, ASP.NET, ASP.NET MVC, or Silverlight. At Syncfusion, we uncompromisingly strive for excellence in order to offer the very best value to our customers—from small ISVs to Fortune 100 companies. Our most successful product is Essential Studio.



        </div>

    </div> 



@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableFade(false).EnableNativeScrolling(false).ShowScrollbars(true)


{% endhighlight %}

The following screenshot displays “show scrollbars”:



![](Show-Scrollbars_images/Show-Scrollbars_img1.png)



