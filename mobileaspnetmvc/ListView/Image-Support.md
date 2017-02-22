---
layout: post
title: image-support
description: image support
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: image
---

## Image support

You can add images to your ListView items by specifying the "ImageUrl" attribute.

The following code example displays how to add images to the ListView.

{% highlight html %}

        @Html.EJMobile().ListView("listview").Items(items =>
   {
       items.Add().Text("Australia").ImageUrl("Australia.png");
       items.Add().Text("Brazil").ImageUrl("Brazil.png");
       items.Add().Text("China").ImageUrl("china.png");
       items.Add().Text("India").ImageUrl("India.png");
       items.Add().Text("Spain").ImageUrl("Spain.png");
   })


{% endhighlight %}

![](image-support_images\image-support_img1.png)

