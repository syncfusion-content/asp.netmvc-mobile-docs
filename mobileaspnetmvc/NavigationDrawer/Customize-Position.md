---
layout: post
title: Customize-Position
description: customize position
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

## Customize Position

Position property is used to specify the position whether it is fixed or relative to the container. When you specify its position as normal, it appends within the container otherwise it appends to the appview.

Refer to the following code examples. 



@{   @Html.EJMobile().NavigationDrawer("navpane").Position(NavigationDrawerPosition.Normal).EnableListView(true).ListViewSettings(list =>

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

    &lt;div id="content" style="margin-top: 45px;"&gt;

        &lt;div id="Home"&gt;

                The Home screen allows you to choose the specific content type displayed.



        &lt;/div&gt;

        &lt;div id="Profile" style="display: none"&gt;

            The Profile page content is displayed.

        &lt;/div&gt;



        &lt;div id="Photos" style="display: none"&gt;

            The Photos page content is displayed.

        &lt;/div&gt;



        &lt;div id="Location" style="display: none"&gt;

            The Location page content is displayed.

        &lt;/div&gt;

    &lt;/div&gt;



}





Refer to the script section to update the page content while clicking the item in the drawer.

