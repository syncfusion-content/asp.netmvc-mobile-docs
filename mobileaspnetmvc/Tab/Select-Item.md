---
layout: post
title: Select-Item
description: select item
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

# Select Item

Tab control takes a numeric value given in selectedItemIndex property and selects the corresponding item that matches the given index. Default value for SelectedItemIndex property is set to 0. You can refer the following code example. 

{% highlight html %}

@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).SelectedItemIndex(1).Items(item =>{

item.Add().Text("My Music").Href("#mymusic").IOS7(ios7=>ios7.ImageClass("icn-Mymusic"));

item.Add().Text("Favorites").Href("#favorites").IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

item.Add().Text("Updates").Href("#updates").IOS7(ios7 => ios7.ImageClass("icn-Updates"));

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })

{% endhighlight %}

The following screenshot displays the Selected Items:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab5.png](Select-Item_images/Select-Item_img1.png)



