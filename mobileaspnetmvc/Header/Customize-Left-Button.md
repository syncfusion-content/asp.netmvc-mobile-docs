---
layout: post
title: Customize Left Button| Header and Footer | MobileAspNetMVC | Syncfusion
description: customize left button
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Customize Left Button

## LeftButtonCaption

To specify the caption (text) for the Header left button, set the “leftbuttoncaption” property. By default, the property value is set to back.

{% highlight html %}
@Html.EJMobile().Header("header_sample").ShowLeftButton(true).LeftButtonCaption("Home")
{% endhighlight  %}
The following screenshot displays the Left Button Caption:

![](Customize-Left-Button_images/Customize-Left-Button_img1.png)



## LeftButtonStyle

The LeftButtonStyle property specifies the style of the Header left button.

The possible values are, 

1. Back
2. Header
3. Normal

{% highlight html %}

@Html.EJMobile().Header("header_sample").ShowLeftButton(true).LeftButtonStyle(LeftButtonStyle.Normal)

{% endhighlight  %}
The following screenshot displays the Left Button Style:

![](Customize-Left-Button_images/Customize-Left-Button_img2.png)



## LeftButtonNavigationURL

Specifies the navigation URL of the page while clicking the left button.

{% highlight html %}
@Html.EJMobile().Header("header_sample").ShowLeftButton(true).LeftButtonNavigationUrl("navigation.html")
{% endhighlight  %}


