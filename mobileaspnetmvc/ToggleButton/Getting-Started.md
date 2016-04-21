---
layout: post
title: Getting Started| Toggle Button | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Toggle Button
documentation: ug
---

# Getting Started

This section briefly describes about how to create a Toggle button and how to use it in your application.

## Create your first Toggle Button in MVC

The ASP.NET MVC Mobile Toggle Button functions, to switch On/Off functions such as Wi - Fi, Bluetooth in mobile.

![C:/Users/durga/Pictures/image1.png](Getting-Started_images/Getting-Started_img1.png)



## Create Toggle Button for Settings

The Toggle Button widget is rendered based on the default values for all the properties. You can easily customize Toggle Button control by changing its properties. The following steps explain you to add a Toggle button for the Settings scenario where you can enable or disable Wi-Fi connectivity.

Add the following code to the corresponding Layout.cshtml page.

{% highlight html %}

 <!-- Header control -->

@Html.EJMobile().Header("header").Title("Settings") .Position(MobileHeaderPosition.Normal)

<div>

  @RenderBody()  

</div>

<!-- Scroll Panel control -->

@Html.EJMobile().Scrollpanel("scrollpanel").Target("content")

{% endhighlight %}

To render Toggle Button control, add the following code to the corresponding view page. 

{% highlight html %}

<!-- Toggle Button control -->

<div id="content" style="margin: 25px 30px;">

        <div class="togglesamtext">

            Wi-Fi

        </div>



        <div class="togglesamele" style="float:right">

            @Html.EJMobile().ToggleButton("toggle").ToggleState(true)

        </div>

    </div>

{% endhighlight %}



Execute the above code to render the following output.



![C:/Users/durga/Pictures/image1.png](Getting-Started_images/Getting-Started_img2.png)



## Change Toggle Button rendering state

You can customize the initial Toggle Button rendering state by setting the ToggleState property to false that accepts Boolean value as its argument.

Add the following code to set the ToggleState property.

{% highlight html %}

<!-- Toggle Button control -->

  <div class="togglesamele" style="float: right">

            @Html.EJMobile().ToggleButton("toggle").ToggleState(false)
  </div>

{% endhighlight %}

Execute the above code to render the following output.



![C:/Users/durga/Pictures/image2.png](Getting-Started_images/Getting-Started_img3.png)



## Handle Events

In this application, when the Toggle Button state is changed, a dialog appears to notify the Wi-Fi state is enabled or disabled. This is achieved by using the ClientSideEvents property. Whenever the Toggle Button’s state changes, the Change event is raised. This event is handled by using appropriate functions.

Add the following code to render the dialog when the toggle state is changed.

{% tabs %}
{% highlight html %}

<!-- Toggle Button control -->

<div class="togglesamele" style="float: right">

            @Html.EJMobile().ToggleButton("toggle").ToggleState(false).ClientSideEvents(evt => { evt.Change("showDialog"); })

        </div>





<!--Dialog Control-->

//to create dialog object

@{

    @Html.EJMobile().Dialog("dialog").Mode(DialogMode.Alert).EnableAutoOpen(false).EnableModal(false).LeftButtonCaption("OK").Content((@<div id="alertdlgcontent">Wi-Fi is Enabled</div>)).ClientSideEvents(evt => { evt.ButtonTap("alertClose"); }) 

}

{% endhighlight %}

{% highlight javascript %}

<script>

    function alertClose() {

        $("#alertdlg").ejmDialog("close");    //to close dialog

    }

    function showDialog(args) {

        (args.state) ? $("#alertdlgcontent").html("Wi-Fi is Enabled") :   $("#alertdlgcontent").html("Wi-Fi is Disabled"); //add content to the dialog respective to the state of Toggle Button

        App.activePage.find("#alertdlg").ejmDialog("open");  //to open dialog

    }



</script>

{% endhighlight %}
{% endtabs %}

Execute the above code to render the following output.

![C:/Users/durga/Pictures/image3.png](Getting-Started_images/Getting-Started_img4.png)



