---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Toolbar
documentation: ug
---

# Getting Started

## Create your first Toolbar in MVC

The Essential Studio for ASP.NET MVC Mobile Toolbar provides a single interface to select a command from a collection of commands. It provides template support. In this example, you can learn how to create a Mail App and through that you can learn the features of Mobile Toolbar Widget.



{ ![1](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


Create the necessary layout

Create a simple MVC application and paste the following header and scrollpanel layout page content inside the &lt;body&gt; tag of layout.cshtml. Add other templates in the view page for Toolbar creation. To create a MVC Project, add necessary Dll’s and Scripts done with the help of the [MVC-Getting Started Documentation](http://help.syncfusion.com/ug/js/default.htm) for mobile.

     @Html.EJMobile().Header("header").Position(MobileHeaderPosition.Normal).Title("inbox")

    &lt;div id="content"&gt;

        @RenderBody()

    &lt;/div&gt;

@Html.EJMobile().Scrollpanel("scroll").Target("content")

 Add the following code in the corresponding view page.

&lt;!--Add Toolbar control here. --&gt;



&lt;!-- Inbox sample content--&gt;

&lt;div id="mailContent" style="padding: 20px;"&gt;

    <b>From:&lt;/b&gt; websupport@syncfusion.com<br />&lt;br /&gt;

    <b>To:</b>john@abc.com</br>&lt;br /&gt;

 <b>SUB:&lt;/b&gt; Your Syncfusion Metro Studio Order 261234 submitted<br />&lt;br /&gt;

    &lt;p&gt;

        Dear Customer,&lt;br /&gt;&lt;br /&gt;

        Thank you for requesting a free license to use Syncfusion Metro Studio. The license provided is perpetual, subject to the terms of our license agreement.

    &lt;/p&gt;

&lt;/div&gt;



@Html.EJMobile().Dialog("alertdlg").Title("Dialog").LeftButtonCaption("OK").ClientSideEvents(c => c.ButtonTap("alertClose"))



Execute this code to render the following output.

{ ![2](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


Create Toolbar Control

To render the Toolbar control, add the following code and include a list of Toolbar items to be added. There are 20 built-in icons for Toolbar items. This can be achieved by using the IconName property.

@Html.EJMobile().Toolbar("toolbar") .Position(Position.Normal) .Android(android=>android.Position(AndroidToolbarPosition.Fixed) .Title("Inbox")).Windows(windows=>windows.Position(WindowsToolbarPosition.Fixed)).Items(item =>

            {

                item.Add().IconName(IconName.Back);

                item.Add().IconName(IconName.Next);

                item.Add().IconName(IconName.Compose);

                item.Add().IconName(IconName.Delete);

                item.Add().IconName(IconName.Close);

            })

 Use the following styles for content style.

        &lt;style&gt;

           .e-m-header.e-m-android {

               display: none;

           }

      &lt;/style&gt;

 Execute this code to render the following output.



{ ![1](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }


Add Functionalities for toolbar items 

You can provide functionalities for each Toolbar items and this can be achieved by adding TouchEnd event. When you click the Toolbar item, its corresponding TouchEnd event triggers and it is handled using the performAction function as shown in the following code example. 

@Html.EJMobile().Toolbar("toolbar").ClientSideEvents(c => c.TouchEnd("performAction")).Position(Position.Normal) .Android(android=>android.Position(Position.Fixed)).Windows(windows=>windows.Position(Position.Fixed)).Items(item =>

            {

                item.Add().IconName(IconName.Back);

                item.Add().IconName(IconName.Next);

                item.Add().IconName(IconName.Compose);

                item.Add().IconName(IconName.Delete);

                item.Add().IconName(IconName.Close);

            })

 &lt;script&gt;

    $(document).ready(function (args) {

        window.dialogObject = $("#alertdlg").data("ejmDialog"); //creating object for dialog

    });

    // toolbar touch end event

    function performAction(args) {

        var itemName = args.itemname;// to get the toolbar item name

        $("#dialogContent").append(itemName + " toolbar item selected."); // appends the content to the dialog

        window.dialogObject.open();// to show dialog

    }

    //Closes dialog

    function alertClose(args) {

        $("#dialogContent").empty(); //empties dialog content

        window.dialogObject.close(); //closes dialog

    }

&lt;/script&gt;

  Execute this code to render the following output.

{ ![3](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }


