---
layout: post
title: Button-Customization
description: button customization
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

## Button Customization

### LeftButtonCaption

The LeftButtonCaption property is used to specify the text of the Left Button. The default value is cancel.



@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").LeftButtonCaption("Ok").EnableAutoOpen(true).Mode(DialogMode.Confirm).Content(

@&lt;div&gt;

Turn on cellular data or use Wi-Fi to access data

&lt;/div&gt;)

}



The following screenshot displays the output.



{ ![](Button-Customization_images/Button-Customization_img1.png) | markdownify }
{:.image }


### RightButtonCaption

The RightButtonCaption property specifies the text of the Right Button. The default value is continue.



@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").RightButtonCaption("Continue").EnableAutoOpen(true).Mode(DialogMode.Confirm).Content(

@&lt;div&gt;

Turn on cellular data or use Wi-Fi to access data

&lt;/div&gt;)

}



The following screenshot displays the output.

{ ![](Button-Customization_images/Button-Customization_img2.png) | markdownify }
{:.image }


### ShowButtons                                

The ShowButtons property is used to show the buttons in the Dialog box. The default value is true.



@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome to Syncfusion").RightButtonCaption("Continue").EnableAutoOpen(true).ShowButtons(false).Mode(DialogMode.Confirm).Content(

@&lt;div&gt;

Syncfusion provides software components and tools for the Microsoft .NET platform

&lt;/div&gt;)

}



The following screenshot displays the output.

{ ![](Button-Customization_images/Button-Customization_img3.png) | markdownify }
{:.image }


