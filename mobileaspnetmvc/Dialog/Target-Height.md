---
layout: post
title: Target-Height
description: target height
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

## Target Height

The TargetHeight property specifies the target height of the Dialog.



@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome to Syncfusion").LeftButtonCaption("Cancel").TargetHeight(500).Content(

@<div>

Syncfusion provides software components and tools for the Microsoft .NET platform

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>



[Script]



        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }



The following screenshot displays the output.

{{ '![](Target-Height_images/Target-Height_img1.png)' | markdownify }}
{:.image }


