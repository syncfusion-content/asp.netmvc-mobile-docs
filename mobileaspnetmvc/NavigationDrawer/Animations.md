---
layout: post
title: Animations
description: animations
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

## Animations

You can set the transition type of the Navigation Drawer by using Type property. The possible transition types are slide and overlay. 

Slide – Both navigation panel and content page slides towards left/right direction to view the navigation panel items.

Overlay – Only navigation panel slides over the content page to view the navigation panel items that is, part of the content page is hidden under navigation panel.

> _Note: Transition slide type only working with position fixed._

Refer to the following code example.

@Html.EJMobile().NavigationDrawer("navpane").Type(NavigationDrawerType.Slide).EnableListView(true).Position(NavigationDrawerPosition.Fixed).ListViewSettings(list =>

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



        <div id="content" style="margin-top: 45px; margin-left: 20px;">

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





Refer to the script section to update the page content while clicking the item in the drawer.

