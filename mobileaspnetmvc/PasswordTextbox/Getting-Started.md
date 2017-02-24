---
layout: post
title: Getting Started| Password | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Password
documentation: ug
---

# Getting started

This section describes in brief how to create and customize an ASP.NET MVC Mobile Password widget.

## Create your first Password textbox in ASP.NET MVC

Using the following guidelines, you can create a basic login form using the Password Textbox control.

![](Getting-Started_images/Getting-Started_img1.png)



### Create Password Textbox

Create a simple MVC application and add the following NavigationBar and Scroll panel layout page content inside the <body> tag of layout.cshtml. To create an MVC Project, and add necessary Dll’s and Scripts you can refer to [MVC-Getting Started Documentation](http://help.syncfusion.com/js/) for Mobile.  

{% highlight html %}

<!-- header control -->          

@Html.EJMobile().NavigationBar("header").Mode(NavBarMode.Header).Title("Login")

<div id="sample" class="sample">

<div class="container">

<form id="loginForm">

<label>

User Name

</label>

<div>

@Html.EJMobile().TextBox("userName").WatermarkText("User Name")                

</div>

<label>

Password

</label>



<!-- Add Password textbox here -->



<div class="submit">

@Html.EJMobile().Button("submit").Text("Login")

</div>

</form>

</div>

</div>

<!-- ScrollPanel -->
@Html.EJMobile().Scrollpanel("scrollPanel").Target("sample") 



{% endhighlight %}

Add the following code in the corresponding view page to render the Password Textbox control.

{% highlight html %}


<!-- Password textbox -->

<div>
@Html.EJMobile().PassWord("password") 

</div>




{% endhighlight %}

Add the following styles to show the Password control in an order. 

{% highlight css %}

<style>

.error {

color: red;

}



.sample {

display: table;

width: 100%;

}



.submit {

text-align: center;

}



form {

padding: 15px;

}



.container {

display: table-cell;

vertical-align: middle;

}

</style>



{% endhighlight %}

Run this code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img2.png)



## Set Watermark text

The watermark text specifies a short hint that describes the expected value of the input field. This can be achieved by using the “watermarktext” property.

{% highlight html %}

<!-- Password textbox -->

<div>

@Html.EJMobile().PassWord("password").WatermarkText("Password")

</div>

{% endhighlight %}

Run this code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img3.png)



