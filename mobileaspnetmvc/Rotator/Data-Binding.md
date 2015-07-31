---
layout: post
title: Data-Binding
description: data binding
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Data Binding

Essential Studio for ASP.NET MVC Mobile Rotator provides support for data binding. Data binding provides a simple and consistent way for applications to present and interact with data. Elements can be bound to data from a variety of data sources.

Using DataBinding property you can enable the databinding and DataSource is used to get the datasource that holds the Rotator items. Refer to the following code example.



@model List<Images>

{% highlight html %}

<!-- header control -->

@Html.EJMobile().Header("header").Title("Photo Gallery")

<div id="rotatorcontentdefault">

    <div>

        <div class="photo {{:imageUrl}}">

        </div>

    </div>

</div>



<div id="scrollparent">

    @{     @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").DataBinding(true).DataSource(Model);

    }

</div>

{% endhighlight %}



![F:/thangavel/dev/source/Trunk/JSDoc/rotator-1.png](Data-Binding_images/Data-Binding_img1.png)



