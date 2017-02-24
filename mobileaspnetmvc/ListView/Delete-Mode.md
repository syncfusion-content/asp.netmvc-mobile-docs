---
layout: post
title: delete-mode
description: delete mode
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: listview, delete
---

## Delete mode

Enables delete option for each ListView item when swipe left happens to the ListView item.

{% highlight html %}

        @Html.EJMobile().ListView("listview").DeleteMode(ListDeleteMode.Swipe).Items(items =>
   {
       items.Add().Text("Artwork");
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

![](delete-mode_images\delete-mode_img1.png)

