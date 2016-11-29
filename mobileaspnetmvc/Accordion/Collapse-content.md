---
layout: post
title: Collapse Content| Accordion | MobileAspNetMVC | Syncfusion
description: collapse content
platform: mobileaspnetmvc
control: Accordion
keywords: accordion, collapse
documentation: ug
---

# Collapse content

In some cases, you may want to collapse the Accordion content dynamically due to limited space available in the screen. You can enable this feature by setting “CollapseAll” property to false. By clicking the Accordion header, you can collapse or expand the content.



{% highlight html %}

    @Html.EJMobile().Accordion("accordion_sample").CollapseAll(true).Items(accItem =>
 {

     accItem.Add().Text("MVC").Content(@<div>

        Model-view-controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions

    </div>);

     accItem.Add().Text("WPF").Content(@<div>

        Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications

    </div>);

     accItem.Add().Text("WCF").Content(@<div>

        WCF is a tool often used to implement and deploy a service-oriented architecture (SOA). It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers.  .

    </div>);

 })

{% endhighlight %}

{% highlight html %}


{% endhighlight %}




The following screenshot displays the collapse content:



![](Collapse-content_images/Collapse-content_img1.png)