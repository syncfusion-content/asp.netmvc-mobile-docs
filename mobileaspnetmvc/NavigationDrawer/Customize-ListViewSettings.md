---
layout: post
title: Customize ListViewSettings| Navigation Drawer | MobileAspNetMVC | Syncfusion
description: customize listviewsettings
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

# Customize ListViewSettings

The navigation panel accommodates any template, but most of the use cases requires list view control. So built-in support is provided in Navigation Drawer to render ListView control by setting EnableListView property as true. You can customize all the features available in ListView. For example you can customize the width of the list view.

Refer to the following code example. 

{% highlight html %}

@Html.EJMobile().NavigationDrawer("navpane").EnableListView(true).ListViewSettings(list => {

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



{% endhighlight %}

Refer to the script section to update the page content while clicking the item in the drawer.

The following screenshot illustrates the output.

![](Customize-ListViewSettings_images/Customize-ListViewSettings_img1.png)



