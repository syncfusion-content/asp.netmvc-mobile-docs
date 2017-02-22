---
layout: post
title: Data Binding| Rotator | MobileAspNetMVC | Syncfusion
description: data binding
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Data binding

Essential Studio for ASP.NET MVC Mobile Rotator provides support for data binding. Data binding provides a simple and consistent way for applications to present and interact with data. Elements can be bound to data from a variety of data sources.

DataSource is used to get the datasource that holds the Rotator items. Refer to the following code example.

{% highlight html %}

@model List<Images>



<!-- header control -->

 @Html.EJMobile().NavigationBar("Header").Mode(NavBarMode.Header).Title("Rotator")

<div id="rotatorcontentdefault">

    <div>

        <div class="photo {{:imageUrl}}">

        </div>

    </div>

</div>



<div id="scrollparent">

    @{     @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").DataSource(Model);

    }

</div>

{% endhighlight %}



![](Data-Binding_images/Data-Binding_img1.png)



