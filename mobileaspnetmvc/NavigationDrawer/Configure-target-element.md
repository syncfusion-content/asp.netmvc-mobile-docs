---
layout: post
title: Configure-target-element
description: configure target element
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

## Configure target element

The TargetId property is used to define the target Id for Navigation Drawer. The drawer opens while you click on the specified target element.

Refer to the following code example. 

{% highlight html %}

<div id="target" class="targeticon"></div>      @Html.EJMobile().NavigationDrawer("navpane").TargetId("target").EnableListView(true).ListViewSettings(list =>

{

    list.ClientSideEvents(i => i.TouchEnd("navListClick")).Items(item =>

        {

            item.Add().Text("Home").ImageUrl("http://js.syncfusion.com/UG/Mobile/Content/drawer/home.png");

            item.Add().Text("Profile").ImageUrl("http://js.syncfusion.com/UG/Mobile/Content/drawer/profile.png");

            item.Add().Text("Photos").ImageUrl("http://js.syncfusion.com/UG/Mobile/Content/drawer/photo.png");

            item.Add().Text("Location").ImageUrl("http://js.syncfusion.com/UG/Mobile/Content/drawer/locations.png");

        });

})

@Html.EJMobile().Header("head").Title("NavigationDrawer").Position(MobileHeaderPosition.Normal)



    <div id="content" style="margin-top: 45px;">

        <div id="Home">

              The Home screen allows you to choose the specific content type displayed.



        </div>

        <div id="Profile" style="display: none">

            The Profile page content is displayed.

        </div>



        <div id="Photos" style="display: none">

            The Photos page content is displayed.

        </div>



        <div id="Location" style="display: none">

            The Location page content is displayed.

        </div>

    </div>



    <style>

        .targeticon {

            background: url("http://js.syncfusion.com/UG/Mobile/Content/drawer/sprite.png") no-repeat scroll 0 -344px rgba(0, 0, 0, 0);

            height: 48px;

            left: 10px;

            position: absolute;

            top: 5px;

            width: 48px;

            z-index: 3;

        }

    </style>

{% endhighlight %}

Refer to the script section to update the page content while clicking the item in the drawer.

![](Configure-target-element_images/Configure-target-element_img1.png)



You can display the drawer either by clicking on the target icon or else by swiping from left. Refer to the following screenshot.

![](Configure-target-element_images/Configure-target-element_img2.png)



