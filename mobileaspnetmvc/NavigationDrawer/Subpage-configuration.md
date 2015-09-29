---
layout: post
title: Subpage configuration| Navigation Drawer | MobileAspNetMVC | Syncfusion
description: subpage configuration
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

# Subpage configuration

By default, Navigation Drawer appends to the Appview (Main page). When you set ConsiderSubPage property as true, then the Navigation Drawer appends to its closest subpage. For example, consider that the Navigation Drawer is rendered as a right pane content of splitpane. While opening the application in tablet resolution, normally the Navigation Drawer appends to the appview that is, it appears over the left pane content. In order to make it append in the right pane subpage, you can set this ConsiderSubPage value as true.
Refer to the following code example.



   {% highlight html %}


@{

@Html.EJMobile().NavigationDrawer("navpane").ConsiderSubPage(true).EnableListView(true).ListViewSettings(list =>

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





}

 {% endhighlight %}

Refer to the script section to update the page content while clicking the item in the drawer.

