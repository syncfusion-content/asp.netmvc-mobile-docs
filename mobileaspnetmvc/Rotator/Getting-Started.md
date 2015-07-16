---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Getting Started

In this section, you can learn how to create Rotator for your mobile app.              

## Create your first Rotator in MVC

The Essential Studio for ASP.NET MVC Mobile Rotator widget is a container that helps you to navigate next and previous items through swipe gestures. Each item in Rotator can hold any html content. In the following guideline, you can learn the features in the MobileRotator widget by creating a Photo Gallery App.

{ ![C:/Users/labuser/AppData/Local/Temp/SNAGHTML1f8cc07.PNG](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


Create the required layout

Rotator control is rendered based on the default values of all the properties. You can customize Rotator control by changing its properties according to your requirement.  

Create a simple MVC application and add the following header page content inside the &lt;Body&gt; tag of layout.cshtml. 

You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC-Getting Started Documentation](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) for mobile.

&lt;!-- header control --&gt;

@Html.EJMobile().Header("header").Title("Photo Gallery")

&lt;div id="content"&gt;

    &lt;div&gt;

        @RenderBody()

    &lt;/div&gt;

&lt;/div&gt;



Create the Rotator control

To render the Rotator control, set “TargetId” property with the id of the target element that contains the HTML template for each item. Every first level child &lt;div&gt; element of the target element acts as an item of the Rotator. 

To render the Rotator control, add the following code example.



    &lt;!-- View Page Content --&gt;

&lt;div id="rotatorcontentdefault"&gt;

    &lt;div&gt;       

        &lt;div class="photo photo1"&gt;

        &lt;/div&gt;

    &lt;/div&gt;&lt;div&gt;       

        &lt;div class="photo photo2"&gt;

        &lt;/div&gt;

    &lt;/div&gt;&lt;div&gt;       

        &lt;div class="photo photo3"&gt;

        &lt;/div&gt;

    &lt;/div&gt;&lt;div&gt;       

        &lt;div class="photo photo4"&gt;

        &lt;/div&gt;

    &lt;/div&gt;&lt;div&gt;       

        &lt;div class="photo photo5"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



&lt;!-- Rotator control --&gt;

@Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault") 



Add the following styles to the Rotator items.



&lt;style type="text/css"&gt;

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



&lt;/style&gt;



Execute the above code to render the following output. 

{ ![C:/Users/labuser/Desktop/ac.png](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


Hide the Pager

In the above image, Pager indicates the item that is currently displayed. If you do not want the pager to be displayed,  you can set the ShowPager property to “_false_”.



@Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").ShowPager(false)

Execute the above code to render the following output. 



{ ![C:/Users/labuser/Desktop/b.png](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }




By swiping left and right, you can move to the other images in the Photo Gallery.

{ ![C:/Users/labuser/Desktop/c.png](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }


