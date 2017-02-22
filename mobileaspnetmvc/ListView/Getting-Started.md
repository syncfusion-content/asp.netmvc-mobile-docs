---
layout: post
title: Getting Started| ListView | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: listview , layout
---

# Getting started

This section explains briefly on how to create a ListView control in your ASP.NET MVC application.

## Create your first ListView in MVC

EssentialASP.NET MVC Mobile Listview control builds an interactive listview interface. This control allows you to select an item from a list-like interface and provides the infrastructure to display a set of data items in different layouts or views. Lists display data, data navigation, result lists,and data entry.


Create a simple MVC application and paste the following header in layout page content inside the <body>tag of layout.cshtml. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started).

The following steps help you to add a ListView control for a mobile application that views a list of items such as images, text and navigates to the child item when you click a list item.


![](getting-started_images/Getting-Started_img1.png)


The following steps help you add a ListView control.

## Create basic mobile layout 

Refer [MVC-Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started) to create an MVC Project, add necessary Dll’s and Scripts.

Add the following code inside the <body> tag in the Layout.cshtml page.

{% highlight html %}

< !---Add Header Here  ---> 
 @Html.EJMobile().NavigationBar("header").Title("MailBox")
<div>

    < !---Add ListView control here  ---> 

</div>

{% endhighlight %}

## Create a basic mobile layout

To add Listview control, you need to call ListView helper.                 

 Refer the following code example.

{% highlight html %}

<div id="content">

            @Html.EJMobile().ListView("listview")

            <!-- Add Listview Items Here -->

</div>

{% endhighlight %}

Add the following ListView items,

{% highlight html %}
 @Html.EJMobile().ListView("listview").Items(items =>
   {
       items.Add().GroupTitle("MailBoxes");
       items.Add().Text("Inbox").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
       items.Add().Text("VIP").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
       items.Add().Text("Draft").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
       items.Add().Text("Sent").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
       items.Add().Text("Junk").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
       items.Add().Text("Trash").ImageUrl("http://js.syncfusion.com/ug/mobile/content/listview/sprite.png");
   })

{% endhighlight %}

Add the below style for images

{% highlight css %}

        .e-m-lv-item .e-m-lv-image {
            background-size: 26px 375px;
        }

    
        .e-m-lv-item:nth-child(2) .e-m-lv-image {
            background-position: 8px -87px;            
        }

        .e-m-lv-item:nth-child(3) .e-m-lv-image {
            background-position: 7px -337px;
        }

        .e-m-lv-item:nth-child(4) .e-m-lv-image {
            background-position: 11px -40px;
        }

        .e-m-lv-item:nth-child(5) .e-m-lv-image {
            background-position: 8px -229px;
        }

        .e-m-lv-item:nth-child(6) .e-m-lv-image {
            background-position: 8px 12px;
        }

        .e-m-lv-item:nth-child(7) .e-m-lv-image {
            background-position: 12px -286px;
        }

{% endhighlight %}

Run the above code and you can see the following output.

![](getting-started_images/Getting-Started_img1.png)


