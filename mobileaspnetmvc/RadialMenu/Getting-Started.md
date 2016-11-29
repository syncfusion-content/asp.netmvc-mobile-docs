---
layout: post
title: getting-started
description: getting started
platform: js
control: Radial Menu
keywords: radialmenu
documentation: ug
---

# Getting Started

This section explains briefly on how to create a Radial Menu control in your mobile application.

## Create your first Radial Menu control in MVC


EssentialStudio ASP.NET MVC,Mobile Radial Menu control is a context that represent the menu items in a circular order with a center button element in it. By default, only the center button is visible. The Radial Menu displays the root level menu item with rotational animation effects on clicking the center menu button. You can close it either by clicking on document or by clicking on the center button when the root level items are displayed.

The following steps guide you to add a Radial Menu control for a mobile application. 

## Create basic mobile layout

1. Refer [MVC-Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started) to create a MVC Project, add necessary Dll’s and Scripts.
2. Add the following code in layout.cshtml page to create a header element.
   
{% highlight html %}

 @Html.EJMobile().NavigationBar("header").Title("RadialMenu")
   

{% endhighlight %}
   
## Add Radial Menu control

Refer to the following code example to add a Radial Menu in the corresponding view page. You can specify images for each menu items by setting the ‘ImageURL’ property.

{% highlight html %}



        @Html.EJMobile().RadialMenu("defaultradialmenu").Items(item =>
{
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/music.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/social.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/direction.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/browser.png");
    item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial/ios7/light/message.png");
})


{% endhighlight %}

Run the above code to render the following output. To know how to run the code, refer to this [section](http://help.syncfusion.com/js/).

![](getting-started_images/getting-started_img1.png)



