---
layout: post
title: Ajax-Navigation
description: ajax navigation
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

## Ajax Navigation

EnableAjax

In the ListView widget, when all the items have navigation page to be loaded through Ajax content, then EnableAjax property is set to true. 





@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").EnableAjax(true).ShowHeader(true).HeaderTitle("ListView").Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })

    &lt;style&gt;

        .listrightdiv

        {

            padding:20px;

        }

    &lt;/style&gt;





@*Load1.html*@

&lt;div class="listrightdiv"&gt;      

&lt;span class="subtitlestyle"&gt;<b>Movie Info:&lt;/b&gt;&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      A young boy learns that he has extraordinary powers and is not of this Earth.

      &lt;/div&gt;

&lt;/div&gt;



@*Load2.html*@

&lt;div class="listrightdiv"&gt;

&lt;span class="subtitlestyle"&gt;<b>Movie Info:&lt;/b&gt;&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      The story revolves around United Nations employee Gerry Lane (Pitt).

      &lt;/div&gt;

&lt;/div&gt;



@*Load3.html*@

&lt;div class="listrightdiv"&gt;

&lt;span class="subtitlestyle"&gt;<b>Movie Info:&lt;/b&gt;&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      &lt;/div&gt;

&lt;/div&gt;

The following screenshot displays the Enable Ajax:

{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_1e.png](Ajax-Navigation_images/Ajax-Navigation_img1.png) | markdownify }
{:.image }


{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_2.png](Ajax-Navigation_images/Ajax-Navigation_img2.png) | markdownify }
{:.image }


> _Note: When the Ajax navigation is only for a specific item, then use this property inside item specific configuration. (In JS, use this attribute “data-ej-enableajax” in specific “li” tag in html, while in MVC, set through EnableAjax)._

AjaxSettings

In Ajax method, the ListView widget loads the content with default jQuery settings. You can customize it as in normal Ajax method through AjaxSettings property. The following options are available.

1. Type
2. Cache
3. Async
4. DataType
5. ContentType
6. URL
7. Data





@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").EnableAjax(true).ShowHeader(true).HeaderTitle("ListView").AjaxSettings(ajax => { ajax.Cache(true); }).Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })





@*Load1.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">Man of Steel</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      A young boy learns that he has extraordinary powers and is not of this Earth.

      &lt;/div&gt;

&lt;/div&gt;



@*Load2.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">World War Z</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      The story revolves around United Nations employee Gerry Lane (Pitt).

      &lt;/div&gt;

&lt;/div&gt;



@*Load3.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">Monsters University</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      &lt;/div&gt;

&lt;/div&gt;

The following screenshots display the Ajax Settings:

{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_1e.png](Ajax-Navigation_images/Ajax-Navigation_img3.png) | markdownify }
{:.image }


{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_2.png](Ajax-Navigation_images/Ajax-Navigation_img4.png) | markdownify }
{:.image }


EnableCache

EnableCache is used to prevent loading Ajax content every time. This is set to true only when the content is not updated for each request.





// For MVC, please add 3 cshtml files to the controller and insert the following content to those cshtml files.



@*Sample.cshtml*@

@Html.EJMobile().ListView("ajaxListBox").ShowHeader(false).EnableCache(true).Items(items => {

       items.Add().Text("Man of Steel").Href("Home/Load1");

       items.Add().Text("World War Z").Href("Home/Load2");

       items.Add().Text("Monsters University").Href("Home/Load3");

   })



@*Load1.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">Man of Steel</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      A young boy learns that he has extraordinary powers and is not of this Earth.

      &lt;/div&gt;

&lt;/div&gt;



@*Load2.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">World War Z</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      The story revolves around United Nations employee Gerry Lane (Pitt).

      &lt;/div&gt;

&lt;/div&gt;



@*Load3.cshtml*@

&lt;div class="listrightdiv"&gt;

      <span class="templatetext">Monsters University</span> <span class="subtitlestyle">Movie Info:&lt;/span&gt;

      &lt;div class="subtitlestyle"&gt;

      Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case.

      &lt;/div&gt;

&lt;/div&gt;



