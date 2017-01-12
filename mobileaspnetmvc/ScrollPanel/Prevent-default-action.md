---
layout: post
title: Prevent default action| ScrollPanel | MobileAspNetMVC | Syncfusion
description: prevent default action
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

# Prevent default action

The default action of mouse while dragging over the page is text selection. While using ScrollPanel, you can prevent the default action by using PreventDefault property.  By default, this property is set to true. 

{% highlight html %}



        <div id="content" style="text-align:justify;">
                       London : London, one of the most popular tourist destinations in the world for a reason. A cultural and historical hub, London has an excellent public transportation system that allows visitors to see all the fantastic sights without spending a ton of money on a rental car.
				     London contains four World Heritage Sites.
            paris  : Paris, the city of lights and love - this short guide is full of ideas for how to make the most of the romanticism that oozes from every one of its beautiful corners.You couldn't possibly visit Paris without seeing the Eiffel Tower.
				     Even if you do not want to visit this world famous structure, you will see its top from all over Paris.
    </div>>





@Html.EJMobile().Scrollpanel("sample_scrollpanel").Target("maincontent").EnableNativeScrolling(false).PreventDefault(true)


{% endhighlight %}
