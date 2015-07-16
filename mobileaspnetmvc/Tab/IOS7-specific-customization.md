---
layout: post
title: IOS7-specific-customization
description: ios7 specific customization
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

## IOS7 specific customization

You can set IOS7 specific properties to the control by accessing IOS7 property.

ImageClass 

The ImageClass property is used to add images to the Tab by specifying the ImageClass for individual items in the Tab. 



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).Items(item =>{

item.Add().Text("My Music").Href("#mymusic").IOS7(ios7=>ios7.ImageClass("icn-Mymusic"));

item.Add().Text("Favorites").Href("#favorites").IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

item.Add().Text("Updates").Href("#updates").IOS7(ios7 => ios7.ImageClass("icn-Updates"));

       })

&lt;!-- Tab first item --&gt;

@Html.EJMobile().ListView("mymusic").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

&lt;!-- Tab second item --&gt;

@Html.EJMobile().ListView("favorites").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

&lt;!-- Tab third item --&gt;

@Html.EJMobile().ListView("updates").ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })



To add the images, use the following styles.

&lt;style&gt;

    .icn-Mymusic {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/mymusic.png') no-repeat center center;

    }



    .icn-Updates {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/updates.png') no-repeat center center;

    }



    .e-m-tabitem.e-m-state-default .icn-Mymusic {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/mymusic-default.png') no-repeat center center;

    }



    .e-m-tabitem.e-m-state-default .icn-Updates {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/updates-default.png') no-repeat center center;

    }



    .icn-Favorites {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/favorites.png') no-repeat center center;

    }



    .e-m-tabitem.e-m-state-default .icn-Favorites {

        background: url('http://js.syncfusion.com/UG/Mobile/Content/favorites-default.png') no-repeat center center;

    }



    .e-m-tab.e-m-ios7 .e-m-tab-image {

        width: 26px;

    }



    .e-m-tab-content .e-m-content {

       padding: 0px;

    }



   .e-m-lv .e-m-list .e-m-list-text,.e-m-windows.e-m-lv.e-m-mobile .e-m-list-text {

       left:0px;

    }



   .e-m-lv.e-m-android .e-m-list .e-m-list-text {

       left: 20px;

    }

&lt;/style&gt;



The following screenshot displays ImageClass:

{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/sources/Screen shots/tab2.png](IOS7-specific-customization_images/IOS7-specific-customization_img1.png) | markdownify }
{:.image }


OverflowBadge

In the iOS, when the number of Tab items do not fit the available screen width, it adds a “more” Tab that contains the list of overflowed Tab items as its content. Overflowbadge specifies badge representation for overflowed Tab items (number of updates available in all overflowed Tab items). Set the badge specific properties by means of accessing this property for overflowing Tab items.

Enabled

The Enabled property is used to enable or disable the badge to your overflow Tab item. Default value is set to false.

Value

The Value property is used to set the badge value for the overflow Tab item. Default value is set to 0.



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).IOS7(ios7 => ios7.OverflowBadge(overflow => { 

    overflow.Enabled(true).Value(2); })).Items(item =>

{    

    item.Add().Text("Featured").Href("#favorites").IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

    item.Add().Text("Charts").Href("#charts").IOS7(ios7 => ios7.ImageClass("icn-Charts"));

    item.Add().Text("Explore").Href("#explore").IOS7(ios7 => ios7.ImageClass("icn-Explore"));    

    item.Add().Text("Music").Href("#music").IOS7(ios7 => ios7.ImageClass("icn-Mymusic"));

    item.Add().Text("Updates").Href("#updates").IOS7(ios7 => ios7.ImageClass("icn-Updates"));

    item.Add().Text("Search").Href("#search").IOS7(ios7 => ios7.ImageClass("icn-Search"));

})

&lt;!-- Tab first item --&gt;

@Html.EJMobile().ListView("favorites").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

&lt;!-- Tab second item --&gt;

@Html.EJMobile().ListView("charts").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Facebook");

                item.Add().Text("Skype");

                item.Add().Text("YouTube");                

            })

&lt;!-- Tab third item --&gt;

@Html.EJMobile().ListView("explore").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Find your near Location");

            })

&lt;!-- Tab fourth item --&gt;

@Html.EJMobile().ListView("music").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");                

            })

&lt;!-- Tab fifth item --&gt;

@Html.EJMobile().ListView("updates").ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })

&lt;!-- Tab sixth item --&gt;

@Html.EJMobile().ListView("search").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Search content here");               

            })



The following screenshot displays the Overflow Badge:

{ ![F:/thangavel/dev/source/Trunk/JSDoc/rotator-5.png](IOS7-specific-customization_images/IOS7-specific-customization_img2.png) | markdownify }
{:.image }


MaxValue

The Value property is used to set the maximum badge value to the overflow Tab item. Default value is set to 100.



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).IOS7(ios7 => ios7.OverflowBadge(overflow => { 

    overflow.Enabled(true).Value(2).MaximumValue(1); })).Items(item =>

{    

    item.Add().Text("Featured").Href("#favorites").IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

    item.Add().Text("Charts").Href("#charts").IOS7(ios7 => ios7.ImageClass("icn-Charts"));

    item.Add().Text("Explore").Href("#explore").IOS7(ios7 => ios7.ImageClass("icn-Explore"));    

    item.Add().Text("Music").Href("#music").IOS7(ios7 => ios7.ImageClass("icn-Mymusic"));

    item.Add().Text("Updates").Href("#updates").IOS7(ios7 => ios7.ImageClass("icn-Updates"));

    item.Add().Text("Search").Href("#search").IOS7(ios7 => ios7.ImageClass("icn-Search"));

}) 

&lt;!-- Tab first item --&gt;

@Html.EJMobile().ListView("favorites").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

&lt;!-- Tab second item --&gt;

@Html.EJMobile().ListView("charts").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Facebook");

                item.Add().Text("Skype");

                item.Add().Text("YouTube");                

            })

&lt;!-- Tab third item --&gt;

@Html.EJMobile().ListView("explore").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Find your near Location");

            })

&lt;!-- Tab fourth item --&gt;

@Html.EJMobile().ListView("music").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");                

            })

&lt;!-- Tab fifth item --&gt;

@Html.EJMobile().ListView("updates").ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })

&lt;!-- Tab sixth item --&gt;

@Html.EJMobile().ListView("search").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Search content here");               

            })



The following screenshot displays the MaxValue:

{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/images/ios7_10.png](IOS7-specific-customization_images/IOS7-specific-customization_img3.png) | markdownify }
{:.image }


