---
layout: post
title: Orientation
description: orientation
platform: mobileaspnetmvc
control: Rotator
documentation: ug
---

## Orientation

The Orientation property is used to swipe the Rotator in Horizontal and Vertical direction. By default value of Orientation is Horizontal.

The pager is provided to indicate the item that is currently selected from the available number of items. The ShowPager property is used to show the pager. The PagerPosition property is used to specify the pager position according to Orientation. The PagerPosition possible values are as follows.

For Vertical Orientation

* Left
* Right



For Horizontal Orientation

* Top
* Bottom



Refer to the following code example.



&lt;!-- header control --&gt;

@Html.EJMobile().Header("header").Title("Rotator")



&lt;div id="rotatorcontentdefault"&gt;

    &lt;div&gt;

        &lt;div class="photo photo1"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo2"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo3"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo4"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div&gt;

        &lt;div class="photo photo5"&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



&lt;!-- Rotator control --&gt;

&lt;div id="scrollparent"&gt;

    @{  

@Html.EJMobile().Rotator("rotatordefault").TargetId("rotatorcontentdefault").Orientation(Orientation.Vertical).ShowPager(true).PagerPosition(pager => { pager.PagerPositionVertical(PagerPositionVertical.Left);});

}

&lt;/div&gt;



Add the following styles to the style section. 

> _Note: You can use the following styles for all the other samples explained as follows._



&lt;style type="text/css"&gt;

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

    &lt;/style&gt;



{ ![F:/thangavel/dev/source/Trunk/JSDoc/rotator-4.png](Orientation_images/Orientation_img1.png) | markdownify }
{:.image }


