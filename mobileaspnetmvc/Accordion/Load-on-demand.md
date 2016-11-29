---
layout: post
title: Load On Demand| Accordion | MobileAspNetMVC | Syncfusion
description: load on demand
platform: mobileaspnetmvc
control: Accordion
keywords: accordion, load
documentation: ug
---

# Load on demand

Enable the "EnableAjax" property to load the Ajax content. To achieve this, specify “Href” attribute with the respective URL of the HTML file that contains the dynamic content. The data-ej-spinnertext attribute is used to show the loading text, while getting (waiting for) the response from the server (via Ajax request).




{% highlight html %}
 @{ Html.EJMobile().Accordion("accordion_sample").EnableAjax(true).SpinnerText("Loading..").Items(accItem =>
        {

            accItem.Add().Text("MVC").Href(@Url.Content("~/accordion/text1"));

            accItem.Add().Text("WPF").Href(@Url.Content("~/accordion/text2"));

            accItem.Add().Text("WCF").Href(@Url.Content("~/accordion/text3"));



        }).Render();}

{% endhighlight %}


Create an HTML file with the name text1.html.


{% highlight html %}


<body>

    Model-view-controller (MVC) is a software architecture pattern which separates the

    representation of information from the user's interaction with it.

    The model consists  of application data, business rules, logic, and functions

</body>

{% endhighlight %}


Create an HTML file with the name text2.html.


{% highlight html %}




<body>

    Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a 

    computer-     software graphical subsystem for rendering user interfaces 

    in Windows-based applications.

</body>
{% endhighlight %}


Create an HTML file with the name text3.html.


{% highlight html %}




<body>

    WCF is a tool often used to implement and deploy a service-oriented architecture

    (SOA). It is designed using service-oriented architecture principles to support

    distributed computing where services have remote consumers.

</body>
{% endhighlight %}


The following screenshot displays the load on demand:



![](Load-on-demand_images/Load-on-demand_img1.png)



