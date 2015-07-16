---
layout: post
title: Title
description: title
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

## Title

The Title property is used to display the title text of the Dialog box. 



@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome to Syncfusion").LeftButtonCaption("Cancel").Content(

@&lt;div&gt;

Syncfusion provides software components and tools for the Microsoft .NET platform

&lt;/div&gt;)

}



&lt;div style="text-align: center"&gt;

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

&lt;/div&gt;



[Script]



        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }



The following screenshot displays the output.

{ ![](Title_images/Title_img1.png) | markdownify }
{:.image }


