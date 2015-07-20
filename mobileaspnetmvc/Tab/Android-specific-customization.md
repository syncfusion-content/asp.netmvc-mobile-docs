---
layout: post
title: Android-specific-customization
description: android specific customization
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

## Android specific customization

You can set the Android specific properties to the control by accessing the Android property.

ShowImage

The ShowImage property is used to enable or disable the image to your Tab. Default value is set to false. 



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.Android).Android(android=>android.ShowImage(true)).Items(item =>{

    item.Add().Text("My Music").Href("#mymusic").Android(android => android.ImageClass("icn-Mymusic"));

    item.Add().Text("Favorites").Href("#favorites").Android(android => android.ImageClass("icn-Favorites"));

    item.Add().Text("Updates").Href("#updates").Android(android=>android.ImageClass("icn-Updates"));

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })



The following screenshot displays the Android ShowImage:

{{ '![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab8.png](Android-specific-customization_images/Android-specific-customization_img1.png)' | markdownify }}
{:.image }


ImageClass

The ImageClass is used to add images to the Tab by specifying the ImageClass for individual items in the Tab. 



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.Android).Android(android=>android.

ShowImage(true)).Items(item =>{

    item.Add().Text("My Music").Href("#mymusic").Android(android => 

android.ImageClass("icn-Mymusic"));

    item.Add().Text("Favorites").Href("#favorites").Android(android => 

android.ImageClass("icn-Favorites"));

    item.Add().Text("Updates").Href("#updates").Android(android=>

android.ImageClass("icn-Updates"));

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").RenderMode(RenderMode.Android).

ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").RenderMode(RenderMode.Android).

ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").RenderMode(RenderMode.Android).

ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })



The following screenshot displays the Android ImageClass:

{{ '![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab8.png](Android-specific-customization_images/Android-specific-customization_img2.png)' | markdownify }}
{:.image }


Position

The Position property holds fixed and normal values. Normal position allows relative position of the element to the appview and fixed position allows fixed position of the element. Default position is set to fixed. 



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.Android).Android(android=>android.ShowImage(true).Position(ControlPosition.Normal)).Items(item =>{

    item.Add().Text("My Music").Href("#mymusic").Android(android => android.ImageClass("icn-Mymusic"));

    item.Add().Text("Favorites").Href("#favorites").Android(android => android.ImageClass("icn-Favorites"));

    item.Add().Text("Updates").Href("#updates").Android(android=>android.ImageClass("icn-Updates"));

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").RenderMode(RenderMode.Android).ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })



The following screenshot displays the AndroidPosition:

{{ '![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab8.png](Android-specific-customization_images/Android-specific-customization_img3.png)' | markdownify }}
{:.image }


