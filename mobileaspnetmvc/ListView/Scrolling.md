---
layout: post
title: Scrolling
description: scrolling
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

# Scrolling

The AllowScrolling property defines whether to allow the scrolling behavior of the content when it exceeds the target elements’ height.

{% highlight html %}

@Html.EJMobile().ListView("lb").ShowHeader(true).HeaderTitle("ListView").AllowScrolling(true).Items(items =>

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

Note: Run this code example and you can see the following output. For more details, refer to the "Common Getting Started" section.

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_10.png](Scrolling_images/Scrolling_img1.png)


## EnableNativeScrolling

Even though there is inbuilt mobile JS scroll bar in the ListView, it is also possible to use the Native Scroll Bar based on the device it gets rendered. It is done by adding EnableNativeScrolling property to the ListView element. 

{% highlight html %}

@Html.EJMobile().ListView("lb").AllowScrolling(true).EnableNativeScrolling(true).Items(items =>

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

## AdjustFixedPosition

AdjustFixedPosition is used to render fixed elements and ListView in the same page. When this property is set to true, it automatically calculates and places the ListView without overlaying any element.

The following code example demonstrates how it looks when this property is disabled. Default header in the ListView is disabled and a new header is created with Fixed Position. Since the header is fixed, you have to set the AdjustFixedPosition value to true to adjust its content dynamically.

{% highlight html %}

@Html.EJMobile().Header("header").Position(MobileHeaderPosition.Fixed).Title("ListView")

@Html.EJMobile().ListView("lb").AdjustFixedPosition(true).ShowHeader(false).Items(items =>

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

The following screenshots display the Adjust Fixed Position:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_15.png](Scrolling_images/Scrolling_img2.png)

Note: You can see here that the first list item is hidden due to fixed header element.

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_16.png](Scrolling_images/Scrolling_img3.png)


## CheckDomChanges

CheckDomChanges property specifies the regular updates for scroll bar in the ListView when new item is dynamically added. When this property is enabled, scroll height in the ListView is also adjusted as per the number of items.

{% highlight html %}

@Html.EJMobile().ListView("lb").CheckDomChanges(true).ShowHeader(false).Items(items =>

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

