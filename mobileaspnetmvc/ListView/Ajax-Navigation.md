---
layout: post
title: Ajax-Navigation
description: ajax navigation
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

# Ajax Navigation

## EnableAjax

In the ListView widget, when all the items have navigation page to be loaded through Ajax content, then EnableAjax property is set to true. 

{% highlight html %}

@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").EnableAjax(true).ShowHeader(true).HeaderTitle("ListView").Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })

    <style>

        .listrightdiv

        {

            padding:20px;

        }

    </style>

{% endhighlight %}

{% highlight html %}

@*Load1.html*@

<div class="listrightdiv">      

<span class="subtitlestyle"><b>Movie Info:</b></span>

      <div class="subtitlestyle">

      A young boy learns that he has extraordinary powers and is not of this Earth.

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load2.html*@

<div class="listrightdiv">

<span class="subtitlestyle"><b>Movie Info:</b></span>

      <div class="subtitlestyle">

      The story revolves around United Nations employee Gerry Lane (Pitt).

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load3.html*@

<div class="listrightdiv">

<span class="subtitlestyle"><b>Movie Info:</b></span>

      <div class="subtitlestyle">

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      </div>

</div>

{% endhighlight %}

The following screenshot displays the Enable Ajax:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_1e.png](Ajax-Navigation_images/Ajax-Navigation_img1.png)



![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_2.png](Ajax-Navigation_images/Ajax-Navigation_img2.png)



Note: When the Ajax navigation is only for a specific item, then use this property inside item specific configuration. (In JS, use this attribute “data-ej-enableajax” in specific “li” tag in html, while in MVC, set through EnableAjax).

## AjaxSettings

In Ajax method, the ListView widget loads the content with default jQuery settings. You can customize it as in normal Ajax method through AjaxSettings property. The following options are available.

1. Type
2. Cache
3. Async
4. DataType
5. ContentType
6. URL
7. Data

{% highlight html %}

@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").EnableAjax(true).ShowHeader(true).HeaderTitle("ListView").AjaxSettings(ajax => { ajax.Cache(true); }).Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })

{% endhighlight %}

{% highlight html %}

@*Load1.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">Man of Steel</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      A young boy learns that he has extraordinary powers and is not of this Earth.

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load2.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">World War Z</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      The story revolves around United Nations employee Gerry Lane (Pitt).

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load3.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">Monsters University</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      </div>

</div>

{% endhighlight %}

The following screenshots display the Ajax Settings:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_1e.png](Ajax-Navigation_images/Ajax-Navigation_img3.png)



[C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_2.png](Ajax-Navigation_images/Ajax-Navigation_img4.png)



## EnableCache

EnableCache is used to prevent loading Ajax content every time. This is set to true only when the content is not updated for each request.


// For MVC, please add 3 cshtml files to the controller and insert the following content to those cshtml files.

{% highlight html %}

@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").ShowHeader(false).EnableCache(true).Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })

{% endhighlight %}

{% highlight html %}

@*Load1.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">Man of Steel</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      A young boy learns that he has extraordinary powers and is not of this Earth.

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load2.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">World War Z</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      The story revolves around United Nations employee Gerry Lane (Pitt).

      </div>

</div>

{% endhighlight %}

{% highlight html %}

@*Load3.cshtml*@

<div class="listrightdiv">

      <span class="templatetext">Monsters University</span> <span class="subtitlestyle">Movie Info:</span>

      <div class="subtitlestyle">

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      </div>

</div>

{% endhighlight %}

