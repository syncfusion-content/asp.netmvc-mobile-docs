---
layout: post
title: Configure icons| Toolbar | MobileAspNetMVC | Syncfusion
description: configure icons
platform: mobileaspnetmvc
control: Toolbar
documentation: ug
---

# Configure icons

You can use different icons in your Toolbar and also you can customize these icons for each item by using the IconName property.

The following built-in icons can be used in Toolbar.

1.    Add
2.    Back
3.    Bookmark
4.    Close
5.    Compose
6.    Copy
7.    Cut
8.    Delete
9.    Done
10.   Edit
11.   Mail
12.   Next
13.   Refresh
14.   Overflow
15.   Paste
16.   Reply
17.   Save
18.   Search
19.   Settings
20.   Share



Refer to the following code example.

{% highlight html %}

  @Html.EJMobile().NavigationBar("toolbar").Mode(NavBarMode.Toolbar).Title("toolbar").Items(item =>

    {

        item.Add().IconName("add");
        item.Add().IconName("cut");
        item.Add().IconName("copy");
        item.Add().IconName("save");
        item.Add().IconName("search");
    

    })

{% endhighlight %}

The following screenshot illustrates the output of the above code.

![](Configure-icons_images/Configure-icons_img1.png)





