---
layout: post
title: Pane-Settings
description: pane settings
platform: mobileaspnetmvc
control: SplitPane
documentation: ug
---

# Pane Settings

OverlayLeftPane property is used to enable or disable the left pane in lower resolutions. Its default value is true. You can specify the direction of left pane to get slide over the rightpane by using this OverLayDirection. The possible directions are,

* Left - Left overlay pane gets transition from left side.
* Right - Left overlay pane gets transition from right side.



EnableSwipe property is used to display the leftpane while swiping the screen. When this property is set to false, then you cannot swipe the left pane. 

{% highlight html %}


@Html.EJMobile().SplitPane("splitpane").OverlayLeftPane(true).OverlayDirection(OverlayDirection.Right).EnableSwipe(true).LeftPaneTemplate(@<div>

    @Html.EJMobile().ListView("listview").ClientSideEvents(c=>c.TouchEnd("loadContent")).ShowHeader(false).Items(items =>

   {

       items.Add().Text("Item1");

       items.Add().Text("Item2");

       items.Add().Text("Item3");

       items.Add().Text("Item4");

       items.Add().Text("Item5");

       items.Add().Text("Item6");

   })

    </div>)            

{% endhighlight %}

Refer to the script section and page content section to load the right pane content of appropriate page created.

