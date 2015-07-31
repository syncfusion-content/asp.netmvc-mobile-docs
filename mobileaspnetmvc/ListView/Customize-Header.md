---
layout: post
title: Customize-Header
description: customize header
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

# Customize Header

In the ListView, you can enable the built-in Header support. To show or hide the Header in the ListView, use the ShowHeader property. By default, the ListView is rendered with the Header. You can set the title for the Header by using the HeaderTitle property.

{% highlight html %}

@Html.EJMobile().ListView("lb").ShowHeader(true).HeaderTitle("ListView").Items(items => {    

    items.Add().Text("ArtWork");

    items.Add().Text("Abstract");

    items.Add().Text("2 Acrylic Mediums");

    items.Add().Text("Creative Acrylic");

    items.Add().Text("Modern Painting");

    items.Add().Text("Canvas Art");

    items.Add().Text("Black white");

    items.Add().Text("Children");

    items.Add().Text("Preschool Crafts");

    items.Add().Text("School-age Crafts");

})

{% endhighlight %}

In some cases, for navigation purposes you may want to show Back button in the ListViewHeader. To achieve this, use ShowHeaderBackButton property. By default, the ListView is not rendered with Header Back button in the parent page. To customize the text shown in the ListViewHeader Back button, the HeaderBackButtonText property is used. 

{% highlight html %}

@Html.EJMobile().ListView("lb").ShowHeader(true).HeaderTitle("ListView").ShowHeaderBackButton(true).HeaderBackButtonText("Home").Items(items => {    

    items.Add().Text("ArtWork");

    items.Add().Text("Abstract");

    items.Add().Text("2 Acrylic Mediums");

    items.Add().Text("Creative Acrylic");

    items.Add().Text("Modern Painting");

    items.Add().Text("Canvas Art");

    items.Add().Text("Black white");

    items.Add().Text("Children");

    items.Add().Text("Preschool Crafts");

    items.Add().Text("School-age Crafts");

})

{% endhighlight %}

 The following screenshot displays the Customize Header:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_9.png](Customize-Header_images/Customize-Header_img1.png)

While working with hybrid mobile application development for iOS, Android and Windows Platforms, you do not need to specify show/hide Header for each platform. The x property is used to hide/show Header by its native aspects. For example, in some scenarios, Header may not be needed for Android and Windows Platforms (when tab control is used in an application), but in iOS, Header is needed since the tab is placed at the bottom of the page. Considering these scenarios, this property is provided. Enabling this property hides Header in Android and Windows Platform, and shows only in iOS platform.

{% highlight html %}

@Html.EJMobile().ListView("lb").HideHeaderForUnSupportedDevice(true).Items(items =>

{    

    items.Add().Text("ArtWork");

    items.Add().Text("Abstract");

    items.Add().Text("2 Acrylic Mediums");

    items.Add().Text("Creative Acrylic");

    items.Add().Text("Modern Painting");

    items.Add().Text("Canvas Art");

    items.Add().Text("Black white");

    items.Add().Text("Children");

    items.Add().Text("Preschool Crafts");

    items.Add().Text("School-age Crafts");

})

{% endhighlight %}

