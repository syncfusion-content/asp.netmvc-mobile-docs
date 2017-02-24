---
layout: post
title: selection
description: selection
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: selection
---

# Selection

## Multi selection

ListView has a check list feature that is used to select multiple list items, by using set EnableCheckList property as true.

{% highlight html %}


        @Html.EJMobile().ListView("listview").EnableChecklist(true).Items(items =>
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



The following screenshot displays Multiselection:

![](selection_images\selection_img1.png)

## Allow selection

When a specific list item is selected, it is highlighted with an active color. AllowSelection property prevents this behavior when set to false. 

{% highlight html %}


        @Html.EJMobile().ListView("listview").AllowSelection(false).Items(items =>
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



## Persist selection

PersistSelection property is used to highlight the selected item in the ListView control even after touch end happens. By default, the active state is removed once touch end happens.

{% highlight html %}

        @Html.EJMobile().ListView("listview").PersistSelection(true).Items(items =>
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



![](selection_images\selection_img2.png)

