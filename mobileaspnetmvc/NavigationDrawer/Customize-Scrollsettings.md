---
layout: post
title: Customize-Scrollsettings
description: customize scrollsettings 
platform: mobileaspnetmvc
control: Navigation Drawer
documentation: ug
---

# Customize Scrollsettings 

Built-in scrolling support is provided to enable scrolling, when the number of items in the navigation panel exceeds the device height. It can be enabled by setting AllowScrolling property as true. You can customize all the properties of scroll panel control to render in Navigation Drawer. For example by setting ShowScrollbars property as false, you can hide the scrollbar in Navigation Drawer.

Refer to the following code example. 


{% highlight html %}

@Html.EJMobile().NavigationDrawer("navpane").ScrollSettings(scrol => { scrol.ShowScrollbars(false); }).AllowScrolling(true).EnableListView(true).ListViewSettings(list =>{

    list.ClientSideEvents(i => i.TouchEnd("navListClick")).Items(item =>

        {

            item.Add().Text("Home");

            item.Add().Text("Profile");

            item.Add().Text("Photos");

            item.Add().Text("Location");

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


### Script Section

You can update the content and close the Navigation Drawer, once the item is selected from the list.

Refer to the following code example.

{% highlight js %}

    <script>

    function navListClick(args) //To Handle the touch end event

    {

        $('#Home, #Profile, #Photos, #Location').hide(); 

        //Hiding all other contents

        $('#' + args.text).show(); 

        //Displaying the content based on the text of item selected

        $('#navpane').ejmNavigationDrawer('close');

    }

    </script>

{% endhighlight %}

