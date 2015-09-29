---
layout: post
title: Load on demand| Tab | MobileAspNetMVC | Syncfusion
description: load on demand
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

# Load on demand

In some applications, the content for the specific Tab item is loaded only when it is required. By specifying “EnableAjax” property to true and specifying the external URL (via href property), you can load individual items on demand in the Tab. Default value is set to false

{% highlight html %}

@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).Items(item =>{

    item.Add().Text("My Music").Href("Home/mymusic").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Mymusic"));

    item.Add().Text("Favorites").Href("Home/favorites").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

    item.Add().Text("Updates").Href("Home/updates").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Updates"));

       })

{% endhighlight %}

Create an HTML file with title mymusic.html and add the following code example to it.

{% highlight html %}

<!DOCTYPE html>

<html>

<head>

<title>Tab-Mymusic</title>

</head>

<body>

<div data-role="ejmlistview" data-ej-showheader="false" id="mymusic">

    <ul>

        <li data-ej-text="Not Afraid"></li>

        <li data-ej-text="Get Lucky"></li>

        <li data-ej-text="Roar"></li>

        <li data-ej-text="Till I Collapse"></li>

    </ul>

</div>

</body>

</html>

{% endhighlight %}

Create a HTML file with the title favorites.html and add the following code example to it.

{% highlight html %}

<!DOCTYPE html>

<html>

<head>

<title>Tab-Favorites</title>

</head>

<body>

<div data-role="ejmlistview" data-ej-showheader="false" id="favorites">

    <ul>

        <li data-ej-text="Dark Horse"></li>

        <li data-ej-text="Roar"></li>

    </ul>

</div>

</body>

</html>

{% endhighlight %}

Create a HTML file with the title updates.html and add the following code example to it.

{% highlight html %}

<!DOCTYPE html>

<html>

<head>

<title>Tab-Updates</title>

</head>

<body>

<div data-role="ejmlistview" data-ej-showheader="false" id="updates">

 <ul>

     <li data-ej-text="New songs available for download"></li>

     <li data-ej-text="1.2.1 update available"></li>

 </ul>

</div>

</body>

</html>

{% endhighlight %}

