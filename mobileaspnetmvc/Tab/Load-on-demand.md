---
layout: post
title: Load-on-demand
description: load on demand
platform: mobileaspnetmvc
control: Tab
documentation: ug
---

## Load on demand

In some applications, the content for the specific Tab item is loaded only when it is required. By specifying “EnableAjax” property to true and specifying the external URL (via href property), you can load individual items on demand in the Tab. Default value is set to false



@Html.EJMobile().Tab("tab").RenderMode(RenderMode.IOS7).Items(item =>{

    item.Add().Text("My Music").Href("Home/mymusic").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Mymusic"));

    item.Add().Text("Favorites").Href("Home/favorites").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Favorites"));

    item.Add().Text("Updates").Href("Home/updates").EnableAjax(true).IOS7(ios7 => ios7.ImageClass("icn-Updates"));

       })



Create an HTML file with title mymusic.html and add the following code example to it.

&lt;!DOCTYPE html&gt;

&lt;html&gt;

&lt;head&gt;

<title>Tab-Mymusic</title>

&lt;/head&gt;

&lt;body&gt;

&lt;div data-role="ejmlistview" data-ej-showheader="false" id="mymusic"&gt;

    &lt;ul&gt;

        &lt;li data-ej-text="Not Afraid"&gt;&lt;/li&gt;

        &lt;li data-ej-text="Get Lucky"&gt;&lt;/li&gt;

        &lt;li data-ej-text="Roar"&gt;&lt;/li&gt;

        &lt;li data-ej-text="Till I Collapse"&gt;&lt;/li&gt;

    &lt;/ul&gt;

&lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;



Create a HTML file with the title favorites.html and add the following code example to it.

&lt;!DOCTYPE html&gt;

&lt;html&gt;

&lt;head&gt;

<title>Tab-Favorites</title>

&lt;/head&gt;

&lt;body&gt;

&lt;div data-role="ejmlistview" data-ej-showheader="false" id="favorites"&gt;

    &lt;ul&gt;

        &lt;li data-ej-text="Dark Horse"&gt;&lt;/li&gt;

        &lt;li data-ej-text="Roar"&gt;&lt;/li&gt;

    &lt;/ul&gt;

&lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;



Create a HTML file with the title updates.html and add the following code example to it.

&lt;!DOCTYPE html&gt;

&lt;html&gt;

&lt;head&gt;

<title>Tab-Updates</title>

&lt;/head&gt;

&lt;body&gt;

&lt;div data-role="ejmlistview" data-ej-showheader="false" id="updates"&gt;

 &lt;ul&gt;

     &lt;li data-ej-text="New songs available for download"&gt;&lt;/li&gt;

     &lt;li data-ej-text="1.2.1 update available"&gt;&lt;/li&gt;

 &lt;/ul&gt;

&lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;



