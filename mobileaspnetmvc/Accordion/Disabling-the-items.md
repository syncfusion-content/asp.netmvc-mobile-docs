---
layout: post
title: Disabling The Items| Accordion | MobileAspNetMVC | Syncfusion
description: disabling the items
platform: mobileaspnetmvc
control: Accordion
keywords: accordion, disableditems
documentation: ug
---

# Disabling the items

DisabledItems property is used to disable one or more specified items by using its index that can be given as an array.




{% highlight html %}

@Html.EJMobile().Accordion("accordion_sample").DisabledItems(new int[] {1}).Items(accItem =>
 {

     accItem.Add().Text("MVC").Content(@<div>

        Model-view-controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions

    </div>);

     accItem.Add().Text("WPF").Content(@<div>

        Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications.

    </div>);

     accItem.Add().Text("WCF").Content(@<div>

        WCF is a tool often used to implement and deploy a service-oriented architecture (SOA). It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers.

    </div>);
{% endhighlight %}


The following screenshot displays disabling items:

![](Disabling-the-items_images/Disabling-the-items_img1.png)



