---
layout: post
title: Getting Started| Rating | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Rating
keywords: rating
documentation: ug
---

# Getting started

## Create your first Rating control in MVC

The ASP.NET MVC, Mobile Rating Control provides an intuitive Rating experience that allows you to select a number of stars that represent a Rating.


![](Getting-Started_images/Getting-Started_img1.png)



## Create the necessary layout

The following steps guide you to add a Rating control for a mobile application. In this scenario, Rating control is used to rate Google Search mobile app. 

1. Create a simple MVC application and add the following header page content inside the body tag of layout.cshtml. 
2. Creating a MVC Project and adding necessary Dll’s and Scripts is done with the help of the [MVC-Getting Started](https://help.syncfusion.com/aspnetmvc/getting-started) Documentation.
   
{% highlight html %}
   @Html.EJMobile().NavigationBar("header").Title(" Google Search")

<div>
    @*Render Rating control*@
</div>

{% endhighlight %}
   


3. Add the following template to the corresponding view page to create Rating control for this scenario.
   
{% highlight html %}
    <div id="content">
        <div align="center" id="form" style="margin: 20px;">
            <div id="image">
                <!-- to display the google image -->
            </div>
            <div style="padding: 0 20px;">
                <h2>
                    Description
                </h2>
                 Google Search provides many different options for customized search in easiest way.
                <br /><br />
                <h2>
                    Rate Me
                </h2>
            </div>
            <!-- Need to render rating here -->
        </div>
        <!-- Scroll panel -->
        <div data-role="ejmscrollpanel" data-ej-target="content">
        </div>
    </div>
<style>
    #image {
        background: url("http://js.syncfusion.com/UG/Mobile/Content/google.png") no-repeat;
        height: 140px;
        width: 140px;
        margin-top: 50px;
    }

    #form h2 {
        font-weight: bold;
    }
   
{% endhighlight %}

## Adding Rating control

1. To add a Rating control you need to call “Rating” helper. Initially MobileRating control is rendered with default values of all the properties and you can easily customize MobileRating control by changing their properties according to your requirement.  
   
{% highlight html %}
   
		@Html.EJMobile().Rating("rating")
        
{% endhighlight %}
   


2. Execute this code to render a Rating control to rate the application by selecting the stars. For more details, to run the samples refer "Common Getting Started" section.



   ![](Getting-Started_images/Getting-Started_img1.png)



## Set precision

You can customize the Rating precision based on your requirement. You can achieve this by setting the Precision property that allows you to rate more precisely. 

The Rating control supports three precision modes as follows. 

1. In full precision, you can rate the item with complete precise (Example: 1, 2). 
2. In half precision, you can rate the item with half precise (Example: 1.5, 2.5) instead of complete precise. 
3. In exact precision, you can rate the item with exact precise (Example: 3.2, 4.6). In this scenario, you can set the precision mode to Exact.

{% highlight html %}

		 @Html.EJMobile().Rating("rating").Precision(Precision.Exact).Value(2)


{% endhighlight %}
   

![](Getting-Started_images/Getting-Started_img2.png)



