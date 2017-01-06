---
layout: post
title: Getting Started | NavigationBar | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control:  NavigationBar (Mobile)
documentation: ug
keywords: navigationbar
---

# Getting Started

## Create your first NavigationBar in JavaScript

The ASP.NET MVC mobile Toolbar provides a single interface to select a command from a collection of commands. It also provides template support. In this example, you can learn how to create a Mail App and through that you can learn the features of Mobile Toolbar Widget.



![](Getting-Started_images/Getting-Started_img1.png)

## Create the necessary layout

The ASP.NET MVC Mobile NavigationBar  Control  created by using number of <ul> and <li>. Each <li> item performs individual actions. You can customize the NavigationBar control by changing its properties according to your requirement. 


Create a simple MVC application and paste the following header in layout page content inside the <body>tag of layout.cshtml. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started).

{% highlight html %}

        @Html.EJMobile().NavigationBar("header").Title("Inbox")
    </div>
    <div class="sample">
        <!-- Content that needs to be scrolled-->
        <div>

            <!--Adding Inbox sample content-->

            <div id="mailContent" style="padding: 20px;">

                <span>From:</span> websupport@syncfusion.com<br />

                <span>To:</span>john@abc.com<br />

                <span>SUB:</span> Your Syncfusion Metro Studio Order 261234 submitted<br />

                <br />

                <p>

                    Dear Customer,<br />

                    Thank you for requesting a free license to use Syncfusion Metro Studio. The license provided is perpetual, subject to the terms of our license agreement.

                </p>

            </div>

            <!—Adding dialog control -->

            <div id="alertdlg" data-role="ejmdialog" data-ej-title="Dialog"
                 data-ej-leftbuttoncaption="OK" data-ej-buttontap="alertClose">

                <div id="dialogContent">

                </div>

            </div>

        </div>

    </div>

    <div data-role="ejmscrollpanel" data-ej-target="content"></div>

</div>

{% endhighlight %}

Execute this code to render the following output.

![](Getting-Started_images/Getting-Started_img1.png)



