---
layout: post
title: Getting Started| Checkbox | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Checkbox
documentation: ug
---

# Getting Started

This section briefly describes about how to create and customize ASP.NET MVC Mobile Checkbox widget.

## Create your first Checkbox in ASP.NET MVC

From the following guidelines, you can select Multiple or Single Selection List by using Checkbox. The following screenshot demonstrates the functionality with Checkbox button action.

![C:/Users/apoorvah.ramanathan/Desktop/1.png](Getting-Started_images/Getting-Started_img1.png)



In the above screenshot, you can select multiple search engines as your favorites by using Checkbox, Tri-State Checkbox and perform the action to render the checked values when the button is clicked.

### Create Checkbox 

Essential ASP.NET MVC Mobile Checkbox widget has built-in features like indeterminate selections. You can easily create the Checkbox widget by using Html helper codes as follows. 

Create a simple MVC application and add the following header and scrollpanel controls inside the <body> tag of layout.cshtml. 

For creating a MVC Project, adding necessary Dll’s and Scripts can be done with help of the [MVC-Getting Started Documentation](http://help.syncfusion.com/js/) for mobile. 


{% highlight html %}

<!-- header control -->          

@Html.EJMobile().Header("header").Title("Search Engines")

        <div id="content">

            <div>

                @RenderBody()

            </div>			

        </div>

<!-- ScrollPanel -->        

@Html.EJMobile().Scrollpanel("scroll").Target("content") 



{% endhighlight %}



Add the following Layout code to the corresponding view page.

{% highlight html %}



<p id="label">Choose Your Favorite Search Engines</p>

    <table id="main">

        <tr>

            <td>

                 @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox1" }).Text("Google").Checked(true)

            </td>

        </tr>

        <tr>

            <td>

                @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox2" }).Text("Yahoo").Checked(true)

            </td>

        <tr />

        <tr>

            <td>

                @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox3" }).Text("Bing")

            </td>

        <tr />

        <tr>

            <td>

                @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox4" }).Text("Wikipedia").Checked(true)

            </td>

        <tr />

        <tr>

            <td>

                @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox5" }).Text("Amazon")

            </td>

        <tr />

        <tr>

            <td>

                @Html.EJMobile().CheckBox("chkbox", new { id = "Checkbox6" }).Text("Twitter")

            </td>

        <tr />

    </table>

    <div class="btnsub">

        <button id="submit" data-role="ejmbutton">SUBMIT</button>

    </div>





{% endhighlight %}



Add the following styles to show the Checkbox control in an order. 


{% highlight css %}

    <style>



        #main, .btnsub, #label  {

            padding: 20px;

        }



        #label  {

            font-weight: bold;

        }



        .btnsub  {

            text-align: center;

        }

    </style>



{% endhighlight %}



Run this code example and you can see the following output.

![C:/Users/apoorvah.ramanathan/Desktop/1.png](Getting-Started_images/Getting-Started_img2.png)



