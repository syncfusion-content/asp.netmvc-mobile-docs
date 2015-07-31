---
layout: post
title: Windows-specific-customization
description: windows specific customization
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

# Windows specific customization

Set the Windows specific properties to the control by accessing this property.

## EnableCustomText

In the Windows phone, by default the Tab title's text is in the lower case irrespective of whatever case is used for the title. To disable this behavior, set the “windows.enablecustomtext”property to true. Default value is set to false. 

{% highlight html %}

@Html.EJMobile().Tab("tab").RenderMode(RenderMode.Windows).Windows(windows=>windows.EnableCustomText(true))

   .Items(item =>{

    item.Add().Text("My Music").Href("#mymusic");

    item.Add().Text("Favorites").Href("#favorites");

    item.Add().Text("Updates").Href("#updates");

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })

{% endhighlight %}

The following screenshot displays window specific customization:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab6.png](Windows-specific-customization_images/Windows-specific-customization_img1.png)



## Position

The Position property holds fixed and normal values. Normal position allows relative position of the element to the appview and fixed position allows fixed position of the element. Default position is set to fixed. 

{% highlight html %}

@Html.EJMobile().Tab("tab").RenderMode(RenderMode.Windows).Windows(windows=>windows.Position(ControlPosition.Normal))

    .Items(item =>{

    item.Add().Text("My Music").Href("#mymusic");

    item.Add().Text("Favorites").Href("#favorites");

    item.Add().Text("Updates").Href("#updates");

       })

<!-- Tab first item -->

@Html.EJMobile().ListView("mymusic").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Not Afraid");

                item.Add().Text("Get Lucky");

                item.Add().Text("Roar");

                item.Add().Text("Till I Collapse");

            })

<!-- Tab second item -->

@Html.EJMobile().ListView("favorites").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("Dark Horse");

                item.Add().Text("Roar");

            })

<!-- Tab third item -->

@Html.EJMobile().ListView("updates").RenderMode(RenderMode.Windows).ShowHeader(false).Items(item =>

            {

                item.Add().Text("New songs available for download");

                item.Add().Text("1.2.1 update available");

            })

{% endhighlight %}

The following screenshot displays the Window Specific Customization Position:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Tab/Tab Complete Doc/Screen shots/tab7.png](Windows-specific-customization_images/Windows-specific-customization_img2.png)



