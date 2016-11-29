---
layout: post
title: Getting Started| TextArea | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: TextArea
keywords: textarea
documentation: ug
---

# Getting Started

This section briefly describes how to create Essential MVC Mobile TextArea widget in a simple mobile application for new mail creation process.

## Create your first TextArea in MVC

From the following guidelines, you can create basic Mail sending form by using the TextArea control.

![](Getting-Started_images/Getting-Started_img1.png)


In the above image, message field is rendered by using the TextArea.


### Create the necessary layout 

Create a simple MVC application and add the following header and scrollpanel layout page content inside the <body> tag of layout.cshtml. To create a MVC Project, add necessary Dll’s and Scripts with the help of [MVC-Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started) for mobile.

Create an HTML file and add the following template to the HTML file.

{% highlight html %}

<!-- header control -->          
@Html.EJMobile().NavigationBar("mailheader").Title("New Message")

<div id="mailcontainer" class="sample">

    <div>

        <span>To</span>

        @Html.EJMobile().TextBox("mailTo")

        <span>Subject</span>

        @Html.EJMobile().TextBox("mailSubject")

        <span>Message</span>
    <!-- Add TextArea elements here -->          

        <div class="submit">

            @Html.EJMobile().Button("submit").Text("Send")

        </div>

    </div>

</div>

<div id="scrollPanel" data-role="ejmscrollpanel" data-ej-target="mailcontainer"></div>

{% endhighlight %}


### Create textarea

Add the following Layout code to the corresponding view page.                                     

{% highlight html %}

    <!-- TextArea element -->
@Html.EJMobile().TextArea("mailMessage")

{% endhighlight %}

Add the following styles to show the TextArea control in an order.

{% highlight css %}

<style>

        .sample {

            padding: 10px 20px;

        }

</style>

{% endhighlight %}



Run this code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img1.png)





