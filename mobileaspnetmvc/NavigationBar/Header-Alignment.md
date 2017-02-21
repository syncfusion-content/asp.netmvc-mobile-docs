---
layout: post
title: Header Text Alignment | NavigationBar| MobileAspNetMVC | Syncfusion
description: header text  alignment
platform: mobileaspnetmvc
control: NavigationBar (Mobile)
documentation: ug
keywords: alignment
---

# Header text alignment

TitleAlignment property is used to change the alignment of the text.The defaut value of TitleAligment property is left

Text Alignment types

* Center

* left

* Right.

{% highlight html %}

    @Html.EJMobile().NavigationBar("header").Title("Rating").TitleAlignment(TitleAlignment.Right)

   <div class="sample">

       @Html.EJMobile().Rating("rating")

    </div>

{% endhighlight %}

The following screenshot displays the Template ID

![](Header-Alignment-images/Header-Alignment-img1.png)