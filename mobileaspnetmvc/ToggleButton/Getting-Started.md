---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Toggle Button
documentation: ug
---

# Getting Started

This section briefly describes about how to create a Toggle button and how to use it in your application.

## Create your first Toggle Button in MVC

The ASP.NET MVC Mobile Toggle Button functions, to switch On/Off functions such as Wi - Fi, Bluetooth in mobile.

{ ![C:/Users/durga/Pictures/image1.png](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


Create Toggle Button for Settings

The Toggle Button widget is rendered based on the default values for all the properties. You can easily customize Toggle Button control by changing its properties. The following steps explain you to add a Toggle button for the Settings scenario where you can enable or disable Wi-Fi connectivity.

1. Add the following code to the corresponding Layout.cshtml page.

 &lt;!-- Header control --&gt;

@Html.EJMobile().Header("header").Title("Settings") .Position(MobileHeaderPosition.Normal)

&lt;div&gt;

          @RenderBody()  

&lt;/div&gt;

&lt;!-- Scroll Panel control --&gt;

@Html.EJMobile().Scrollpanel("scrollpanel").Target("content")



2. To render Toggle Button control, add the following code to the corresponding view page. 

&lt;!-- Toggle Button control --&gt;

        &lt;div id="content" style="margin: 25px 30px;"&gt;

        &lt;div class="togglesamtext"&gt;

            Wi-Fi

        &lt;/div&gt;



        &lt;div class="togglesamele" style="float:right"&gt;

            @Html.EJMobile().ToggleButton("toggle").ToggleState(true)

        &lt;/div&gt;

    &lt;/div&gt;





3. Execute the above code to render the following output.



{ ![C:/Users/durga/Pictures/image1.png](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


Change Toggle Button rendering state

You can customize the initial Toggle Button rendering state by setting the ToggleState property to false that accepts Boolean value as its argument.

Add the following code to set the ToggleState property.

&lt;!-- Toggle Button control --&gt;

  &lt;div class="togglesamele" style="float: right"&gt;

            @Html.EJMobile().ToggleButton("toggle").ToggleState(false)
  &lt;/div&gt;



Execute the above code to render the following output.



{ ![C:/Users/durga/Pictures/image2.png](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }


Handle Events

In this application, when the Toggle Button state is changed, a dialog appears to notify the Wi-Fi state is enabled or disabled. This is achieved by using the ClientSideEvents property. Whenever the Toggle Button’s state changes, the Change event is raised. This event is handled by using appropriate functions.

Add the following code to render the dialog when the toggle state is changed.

&lt;!-- Toggle Button control --&gt;

&lt;div class="togglesamele" style="float: right"&gt;

            @Html.EJMobile().ToggleButton("toggle").ToggleState(false).ClientSideEvents(evt => { evt.Change("showDialog"); })

        &lt;/div&gt;





&lt;!--Dialog Control--&gt;

//to create dialog object

@{

    @Html.EJMobile().Dialog("dialog").Mode(DialogMode.Alert).EnableAutoOpen(false).EnableModal(false).LeftButtonCaption("OK").Content((@<div id="alertdlgcontent">Wi-Fi is Enabled</div>)).ClientSideEvents(evt => { evt.ButtonTap("alertClose"); }) 

}

&lt;script&gt;

    function alertClose() {

        $("#alertdlg").ejmDialog("close");    //to close dialog

    }

    function showDialog(args) {

        (args.state) ? $("#alertdlgcontent").html("Wi-Fi is Enabled") :   $("#alertdlgcontent").html("Wi-Fi is Disabled"); //add content to the dialog respective to the state of Toggle Button

        App.activePage.find("#alertdlg").ejmDialog("open");  //to open dialog

    }



&lt;/script&gt;



Execute the above code to render the following output.

{ ![C:/Users/durga/Pictures/image3.png](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }


