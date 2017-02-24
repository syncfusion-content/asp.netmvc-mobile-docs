---
layout: post
title: Header TemplateId | NavigationBar | MobileAspNetMVC | Syncfusion
description: header templateid
platform: mobileaspnetmvc
control:  NavigationBar(Mobile)
documentation: ug
keywords: template
---

# Header templateid

data-ej-templateid is used to define the ID of the template element where you can specify the content to render in the control.

{% highlight html %}

  @Html.EJMobile().NavigationBar("header").Title("Rating").TemplateID("template")

<div id="template" class="temp">

            @Html.EJMobile().Rating("rating")

        </div>

{% endhighlight %}

The following screenshot displays the Template ID

![](Header-TemplateId_images/Header-TemplateId_img1.png)