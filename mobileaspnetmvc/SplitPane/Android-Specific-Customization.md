---
layout: post
title: Android-Specific-Customization
description: android specific customization
platform: mobileaspnetmvc
control: SplitPane
documentation: ug
---

## Android Specific Customization

You can set the android specific properties to the control by using the following settings.

> _Note: In iOS and windows, header control is used to set the title for both left pane and right panel. But in android, toolbar control is used as per the native user interface guideline._

## Customize Toolbar

ShowToolbar property is used to show/hide the toolbar when the control is rendered in android mode. You can customize toolbar title by using this toolbarSettings property. 

{% highlight html %}

@Html.EJMobile().SplitPane("splitpane").RenderMode(RenderMode.Android).ToolbarSettings(tool=>tool.Android(toolbar=>toolbar.Title("ToolbarHeader"))).LeftPaneTemplate(@<div>

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

Refer to the script section and page content section to load the right pane content of appropriate page created. The following screenshot illustrates the output.

![](Android-Specific-Customization_images/Android-Specific-Customization_img1.png)



Likewise, you can customize all other properties of toolbar using this property. Refer to the complete UG of toolbar to know its properties.

