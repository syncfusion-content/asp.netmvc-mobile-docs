---
layout: post
title: Orientation| Rotator | MobileAspNetMVC | Syncfusion
description: orientation
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

# Orientation

The Orientation property is used to swipe the Rotator in Horizontal and Vertical direction. By default value of Orientation is Horizontal.

The pager is provided to indicate the item that is currently selected from the available number of items. The ShowPager property is used to show the pager. The PagerPosition property is used to specify the pager position according to Orientation. The PagerPosition possible values are as follows.

For Vertical Orientation

* Left
* Right



For Horizontal Orientation

* Top
* Bottom



Refer to the following code example.

{% highlight html %}

<!-- header control -->

 @Html.EJMobile().NavigationBar("Header").Mode(NavBarMode.Header).Title("Rotator")


<div id="rotatorcontentdefault">

    <div>

        <div class="photo photo1">

        </div>

    </div>

    <div>

        <div class="photo photo2">

        </div>

    </div>

    <div>

        <div class="photo photo3">

        </div>

    </div>

    <div>

        <div class="photo photo4">

        </div>

    </div>

    <div>

        <div class="photo photo5">

        </div>

    </div>

</div>
{% endhighlight %}

{% highlight html %}
<!-- Rotator control -->

<div id="scrollparent">

    @{  

        @Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").Orientation(Orientation.Vertical).ShowPager(true).PagerPosition(MobilePagerPosition.Left);

    }

</div>

{% endhighlight %}

Add the following styles to the style section. 

N> You can use the following styles for all the other samples explained as follows.


{% highlight css %}
<style type="text/css">

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

    </style>

{% endhighlight %}

![](Orientation_images/Orientation_img1.png)



