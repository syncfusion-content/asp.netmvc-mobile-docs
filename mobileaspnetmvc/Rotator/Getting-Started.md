---
layout: post
title: Getting Started| Rotator | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Getting started

In this section, you can learn how to create Rotator for your mobile app.              

## Create your first Rotator in MVC

The Essential Studio for ASP.NET MVC Mobile Rotator widget is a container that helps you to navigate next and previous items through swipe gestures. Each item in Rotator can hold any html content. In the following guideline, you can learn the features in the Mobile Rotator widget by creating a Photo Gallery App.

![](Getting-Started_images/Getting-Started_img1.png)



### Create the required layout

Rotator control is rendered based on the default values of all the properties. You can customize Rotator control by changing its properties according to your requirement.  

Create a simple MVC application and add the following header page content inside the <Body> tag of layout.cshtml. 

You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC-Getting Started Documentation](http://help.syncfusion.com/aspnetmvc/captcha/getting-started#create-your-first-captcha-in-aspnet-mvc ) for mobile.

{% highlight html %}

<!-- header control -->

@Html.EJMobile().NavigationBar("Header").Mode(NavBarMode.Header).Title("Photo Gallery")

<div id="content">

    <div>

        @RenderBody()

    </div>

</div>
{% endhighlight %}


## Create the Rotator control

To render the Rotator control, set “TargetId” property with the id of the target element that contains the HTML template for each item. Every first level child <div> element of the target element acts as an item of the Rotator. 

To render the Rotator control, add the following code example.

{% highlight html %}

    <!-- View Page Content -->

<div id="rotatorcontentdefault">

    <div>       

        <div class="photo photo1">

        </div>

    </div><div>       

        <div class="photo photo2">

        </div>

    </div><div>       

        <div class="photo photo3">

        </div>

    </div><div>       

        <div class="photo photo4">

        </div>

    </div><div>       

        <div class="photo photo5">

        </div>

    </div>

</div>

{% endhighlight %}

{% highlight html %}

<!-- Rotator control -->

@Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault") 

{% endhighlight %}

Add the following styles to the Rotator items.


{% highlight css %}
<style type="text/css">

        .photo {

            background-position: center center;

            background-repeat: no-repeat;

            height: 100%;

            width: 100%;

            background-size:contain;

        }



        .photo1 {

            background-image: url(http://js.syncfusion.com/UG/Mobile/Content/rotator/tablet.jpg);

        }



        .photo2 {

            background-image: url(http://js.syncfusion.com/UG/Mobile/Content/rotator/rose.jpg);

        }



        .photo3 {

            background-image: url(http://js.syncfusion.com/UG/Mobile/Content/rotator/green.jpg);

        }



        .photo4 {

            background-image: url(http://js.syncfusion.com/UG/Mobile/Content/rotator/nature.jpg);

        }



        .photo5 {

            background-image: url(http://js.syncfusion.com/UG/Mobile/Content/rotator/snowfall.jpg);

        }

#content {

        height:500px;

        width:300px;

        margin:auto;

    }



</style>

{% endhighlight %}


Execute the above code to render the following output. 

![](Getting-Started_images/Getting-Started_img2.png)



## Hide the Pager

In the above image, Pager indicates the item that is currently displayed. If you do not want the pager to be displayed,  you can set the ShowPager property to “_false_”.

{% highlight html %}

@Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").ShowPager(false)

{% endhighlight %}

Execute the above code to render the following output. 



![](Getting-Started_images/Getting-Started_img3.png)





By swiping left and right, you can move to the other images in the Photo Gallery.

![](Getting-Started_images/Getting-Started_img4.png)



