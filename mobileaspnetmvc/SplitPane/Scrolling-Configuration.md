---
layout: post
title: Scrolling-Configuration
description: scrolling configuration
platform: mobileaspnetmvc
control: SplitPane
documentation: ug
---

## Scrolling Configuration

RightPane Scroll Settings

The AllowRightPaneScrolling property is used to enable/disable the right pane content scrolling. By default the property is set to true. You can customize the right pane scrolling behavior by using this RightPaneScrollSettings property. 

@Html.EJMobile().SplitPane("splitpane").RightPaneScrollSettings(right=>right.TargetWidth(200)).LeftPaneTemplate(@&lt;div&gt;

    @Html.EJMobile().ListView("listview").ClientSideEvents(c=>c.TouchEnd("loadContent")).ShowHeader(false).Items(items =>

   {

       items.Add().Text("Item1");

       items.Add().Text("Item2");

       items.Add().Text("Item3");

       items.Add().Text("Item4");

       items.Add().Text("Item5");

       items.Add().Text("Item6");

   })

    &lt;/div&gt;)            





Refer to the script section and page content section to load the right pane content of appropriate page created.

Likewise, you can customize all other properties of scrollpanel using this property. Refer to the complete UG of scrollpanel to know its properties.

LeftPane Scroll Settings

The AllowLeftPaneScrolling property is used to enable/disable the left pane content scrolling. By default the property is set to true. You can customize the left pane scrolling behavior by using this LeftPaneScrollSettings property. 

@Html.EJMobile().SplitPane("splitpane").LeftPaneScrollSettings(left=>left.TargetWidth(320)).LeftPaneTemplate(@&lt;div&gt;

    @Html.EJMobile().ListView("listview").ClientSideEvents(c=>c.TouchEnd("loadContent")).ShowHeader(false).Items(items =>

   {

       items.Add().Text("Item1");

       items.Add().Text("Item2");

       items.Add().Text("Item3");

       items.Add().Text("Item4");

       items.Add().Text("Item5");

       items.Add().Text("Item6");

   })

    &lt;/div&gt;)



Refer to the script section and page content section to load the right pane content of appropriate page created. 

Likewise, you can customize all other properties of scrollpanel using this property. Refer to the complete UG of scrollpanel to know its properties.

