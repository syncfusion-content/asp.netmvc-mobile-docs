---
layout: post
title: Android specific customization| Toolbar | MobileAspNetMVC | Syncfusion
description: android specific customization
platform: mobileaspnetmvc
control: Toolbar
documentation: ug
---

# Android specific customization

You can set the Android specific properties to the control by means of accessing Android property.

## Templating

You can customize the Toolbar left side content by using templating feature. This is achieved by setting TemplateId property that specifies the id of the template element.

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().NavigationBar("toolbar_sample").RenderMode(RenderMode.Android).TemplateID("sample1").Items(item =>
   {

      item.Add().IconName("addnew");
      item.Add().IconName("cut");

   })

<span id="sample1">Hi, Welcome</span>

{% endhighlight %}

 The following screenshot illustrates the output of the above code.

![](Android-specific-customization_images/Android-specific-customization_img1.png)



## Split

The Split enum property separates the title and the toolbar items that is displayed at the bottom of the page. You can change the title text by setting the desired title for Title property

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().NavigationBar("toolbar_sample").RenderMode(RenderMode.Android).Items(item =>

   {

        item.Add().IconName("addnew");
        item.Add().IconName("cut");
        item.Add().IconName("copy");

    }).IconAlignment(IconAlignment.Split)

{% endhighlight %}

 The following screenshot illustrates the output of the above code.

![](Android-specific-customization_images/Android-specific-customization_img2.png)










