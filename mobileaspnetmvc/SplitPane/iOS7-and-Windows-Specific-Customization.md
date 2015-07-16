---
layout: post
title: iOS7-and-Windows-Specific-Customization
description: ios7 and windows specific customization
platform: mobileaspnetmvc
control: SplitPane
documentation: ug
---

## iOS7 and Windows Specific Customization

You can set the android and windows specific properties to the control by using the following settings.

LeftHeader settings

You can show/hide the leftpane header by setting the ShowLeftPaneHeader property as true/false. Default value is true.

You can customize the left pane header by using LeftHeaderSettings property. The following code illustrates how to set the title for the left pane

    @Html.EJMobile().SplitPane("splitpane").LeftHeaderSettings(left=>left.Title("Sample Header")).LeftPaneTemplate(@&lt;div&gt;    @Html.EJMobile().ListView("listview").ClientSideEvents(c=>c.TouchEnd("loadContent")).ShowHeader(false).Items(items =>   {

       items.Add().Text("Item1");

       items.Add().Text("Item2");

       items.Add().Text("Item3");

       items.Add().Text("Item4");

       items.Add().Text("Item5");

       items.Add().Text("Item6");

   })

    &lt;/div&gt;)          

Script Section

While selecting an item from the left pane, the corresponding content in right pane is to be loaded. To achieve this, you can handle the touchEnd handler using the loadContent method as follows. 

&lt;script&gt;

    function loadContent() {

        $("#splitpane").ejmSplitPane("loadContent", "splitpane/page");

    }



&lt;/script&gt;

Page Content Section

Add the following code in “page.html” HTML file for right pane. 
The following screenshot illustrates the output for iOS7 and Windows.

iOS7

{ ![](iOS7-and-Windows-Specific-Customization_images/iOS7-and-Windows-Specific-Customization_img1.png) | markdownify }
{:.image }


Windows

{ ![](iOS7-and-Windows-Specific-Customization_images/iOS7-and-Windows-Specific-Customization_img2.png) | markdownify }
{:.image }


Likewise, you can customize all other properties of header. For more reference, check the complete documentation of header. 

RightHeader settings

You can show/hide the right pane header by set as false/true to the ShowRightPaneHeader property. By default the right pane header is displayed, as the ShowRightPaneHeader property is set to true.

You can customize the header related features by using RightHeaderSettings property. The following code illustrates how to set the title for the right pane.  

@Html.EJMobile().SplitPane("splitpane").RightHeaderSettings(header=>header.Title("Page Header")).LeftPaneTemplate(@&lt;div&gt;

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



Refer to the script section and page content section to load the right pane content of appropriate page created. The following screenshot illustrates the output for iOS7 and Windows.

iOS7

{ ![](iOS7-and-Windows-Specific-Customization_images/iOS7-and-Windows-Specific-Customization_img3.png) | markdownify }
{:.image }


Windows

{ ![C:/Users/isuriyar/AppData/Local/Temp/SNAGHTML636b64a.PNG](iOS7-and-Windows-Specific-Customization_images/iOS7-and-Windows-Specific-Customization_img4.png) | markdownify }
{:.image }


Likewise, you can customize all other properties of header. For more reference, check the complete documentation of header.

