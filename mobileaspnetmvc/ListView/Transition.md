---
layout: post
title: Transition
description: transition
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

# Transition

The Transition property is mainly used for the ListView transition effects when navigated from the parent list to the child list and vice-versa. The available transition types are,

1. Slide  
2. Pop
3. Turn

{% highlight html %}

@Html.EJMobile().ListView("lb").Transition("slide").Items(items => {    

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

