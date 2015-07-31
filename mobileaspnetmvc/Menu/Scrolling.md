---
layout: post
title: Scrolling
description: scrolling 	
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Scrolling 	

The AllowScrolling property defines whether to allow the scrolling behavior or not when the number of Menu items exceed the specified Menu height. To display the scrollbars when Allowscrolling is enabled, set the ShowScrollbars property to true. You can customize the height and width of the Menu control by setting the desired value to Height and Width properties respectively. 

{% highlight html %}

    <div style="text-align: center;">

        @Html.EJMobile().Button("menuitem").Text("Menu")

    </div>

    @Html.EJMobile().Menu("menu_sample").TargetId("menuitem").AllowScrolling(true).ShowScrollbars(true).Height(200).Items(item =>

            {

                item.Add().Text("Get info");

                item.Add().Text("Show in folder");

                item.Add().Text("Delete");

                item.Add().Text("Get info");

                item.Add().Text("Show in folder");

                item.Add().Text("Delete");

                item.Add().Text("Get info");

                item.Add().Text("Show in folder");

                item.Add().Text("Delete");

            })
			
{% endhighlight %}

The following screenshot displays Scrolling:

![ShowScrollBars](Scrolling_images/Scrolling_img1.png)



