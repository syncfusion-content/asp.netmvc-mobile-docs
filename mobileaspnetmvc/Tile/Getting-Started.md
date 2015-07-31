---
layout: post
title: Getting-Started
description: getting started 
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

# Getting Started 

## Create your first Tile in MVC

The Essential Studio for ASP.NET MVC Mobile Tiles are simple, opaque rectangles or squares and that are arrayed on the Start screen in a grid-like pattern and it can be either static or live. Tapping or selecting a Tile launches the app or other experience that is represented by the Tile.

![C:/Users/durga/Desktop/Tile1.png](Getting-Started_images/Getting-Started_img1.png)



The following steps guide you in adding a Tile control.

## Creating basic mobile layout

Refer [MVC-Getting Started Documentation](http://help.syncfusion.com/ug/js/default.htm) to create a MVC Project, add necessary Dll’s and Scripts.

Add the following code example in layout page of the application.

{% highlight html %}

    <!-- Add Header Control Here -->

    <div>

           @RenderBody()

    </div>
	
{% endhighlight %}

Add Header control for Tile

Add the following code in layout.cshtml page.

{% highlight html %}

 @Html.EJMobile().Header("header").Title("Tile")

{% endhighlight %}

Add a Tile control

To add a Tile control, call Tile helper. You can set images for Tile by using ImageUrl property.

Add the following code to the corresponding view page.

{% highlight html %}

<div id="tile" style="margin-top: 45px;"> 

@Html.EJMobile().Tile("tile1").Width(50).Height(50).Theme(Theme.Dark).ImageUrl("setting.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Settings") 

    </div>

{% endhighlight %}

Run the above code to render the following output. To know how to run the code, refer to this [section](http://help.syncfusion.com/ug/js/default.htm)

![C:/Users/durga/Desktop/1.png](Getting-Started_images/Getting-Started_img2.png)



## Create Tile as grouped tile

In this scenario, you require different sizes of tiles aligned in a grid-like manner. Here you can add tiles with desired size to make the exact output. The tile gets aligned automatically based on the size it gets rendered. You can define all tiles under the wrapper element with class named ‘group’ to make ‘n’ number of tiles as a grouped tile.

Refer to the following code example.

{% highlight html %}

     <!--Adding Multiple Tiles -->
<div id="tiledefault" class="defaultsample">

  <div id="scrollcontent">

     <div class="group">

       <div class="column">

                @Html.EJMobile().Tile("tile1").Width(50).Height(50).Theme(Theme.Dark).ImageUrl("setting.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Settings")

      <div class="small-col-2">

                    @Html.EJMobile().Tile("tile2").Theme(Theme.Dark).ImageUrl("notes.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Notes")

                    @Html.EJMobile().Tile("tile3").Theme(Theme.Dark).ImageUrl("clock.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Clock")

                    @Html.EJMobile().Tile("tile4").Theme(Theme.Dark).ImageUrl("camera.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Camera")

                    @Html.EJMobile().Tile("tile5").Theme(Theme.Dark).ImageUrl("messaging.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Messages")

                </div>

                @Html.EJMobile().Tile("tile6").Theme(Theme.Dark).ImageUrl("contact.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Contacts")

                @Html.EJMobile().Tile("tile7").Theme(Theme.Dark).ImageUrl("map.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Map")

                @Html.EJMobile().Tile("tile8").Theme(Theme.Dark).ImageUrl("phone.png").ImagePath("http://js.syncfusion.com/UG/Mobile/Content/tile").Text("Phone")

            </div>

        </div>

    </div>

</div>

@Html.EJMobile().Scrollpanel("scroll").Target("scrollcontent")

{% endhighlight %}

Add the following style for setting the background image for all Tiles (page background).

{% highlight css %}

<style>

  .e-m-ios7  .defaultsample

    {

    background: url(" http://js.syncfusion.com/UG/Mobile/Content/tile/bg.png")no-repeat scroll 0 0 / 100% 100% rgba(0, 0, 0, 0);

    height: 100%;

    width: 100%;

     position: absolute;

    }

 </style>

{% endhighlight %}

Run the above code to render the following output. To know how to run the code, refer to this [section](http://help.syncfusion.com/ug/js/default.htm)

![C:/Users/durga/Desktop/Tile1.png](Getting-Started_images/Getting-Started_img3.png)



## Create a grouped tile in Windows Mode

In the windows mode scenario, you require different size of tiles and live tiles. To render the Grouped tile in windows mode, add the following script section, to render the tile with different size and as a live tiles also.

Refer to the following code example.

{% highlight js %}

<script>

  if (ej.getRenderMode() == "windows" || ej.getRenderMode() == "flat") {

            $("#tile1").attr({ 'data-ej-tilesize': 'medium', 'data-ej-text':'People', 'data-ej-imageposition': 'fill' });



            $("#tile2").attr({ 'data-ej-backgroundcolor': ' rgb(208, 75, 43)' });



            $("#tile3").attr({ 'data-ej-livetile-updateinterval': '3500', 'data-ej-livetile-enabled': 'true', 'data-ej-livetile-type': 'flip', 'data-ej-livetile-imageurl': '["clock.png","messaging.png"]', 'data-ej-backgroundcolor': 'rgb(215, 147, 23)' });



            $("#tile4").attr({ 'data-ej-livetile-updateinterval': '3000', 'data-ej-livetile-enabled': 'true', 'data-ej-livetile-type': 'flip', 'data-ej-livetile-imageurl': '["notes.png","camera.png"]', 'data-ej-backgroundcolor': 'rgb(43, 128, 234)' });



            $("#tile5").attr({ 'data-ej-backgroundcolor': 'rgb(94, 58, 179)' });



            $("#tile6").attr({ 'data-ej-tilesize': 'medium', 'data-ej-text': 'Play','data-ej-backgroundcolor': 'rgb(145, 20, 154)' });



            $("#tile7").attr({ 'data-ej-tilesize': 'medium', 'data-ej-text': 'Map','data-ej-backgroundcolor': 'rgb(0, 157, 0)' });



            $("#tile8").attr({ 'data-ej-tilesize': 'wide', 'data-ej-text': 'Sports','data-ej-imageposition': 'fill' });

        }



        if (ej.getRenderMode() == "android")

            $('#scrollcontent').find('div[data-role="ejmtile"]').attr({ 'data-ej-theme': 'light' });



</script>

{% endhighlight %}

