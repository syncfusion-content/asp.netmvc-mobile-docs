---
layout: post
title: Customize Header Icon| Accordion | MobileAspNetMVC | Syncfusion
description: customize header icon
platform: mobileaspnetmvc
control: Accordion
keywords: accordion, expand, collapse
documentation: ug
---

# Customize expand and collapse icon

The “ShowHeaderIcon” property is used to display the expand and collapse icon of the Accordion. By default, header icons are visible. To make the icons invisible, set 'ShowHeaderIcon' to false.

{% highlight html %}

@Html.EJMobile().Accordion("accordion_sample").ShowHeaderIcon(true).Items(accItem =>{

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


The following screenshot displays expand and collapse icon



![](Customize-Header-Icon_images/Customize-expandandcollapse_img1.png)
