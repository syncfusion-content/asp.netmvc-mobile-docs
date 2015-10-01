---
layout: post
title: Customize Right Button| Header and Footer | MobileAspNetMVC | Syncfusion
description: customize right button                                                     
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Customize Right Button                                                     

## RightButtonCaption 

To specify the caption (text) for HeaderRight Button, set “rightbuttoncaption” property. By default, the value is set to “Right”.

{% highlight html %}
@Html.EJMobile().Header("header_sample").ShowRightButton(true).RightButtonCaption("Next")
{% endhighlight  %}
The following screenshot displays the Right Button Caption:

![](Customize-Right-Button_images/Customize-Right-Button_img1.png)



## RightButtonStyle

The RightButtonStyle property is used to specify the style of the Header right button.

The possible values are, 

1. Header
2. Normal


{% highlight html %}
@Html.EJMobile().Header("header_sample").ShowRightButton(true).RightButtonStyle(RightButtonStyle.Header)
{% endhighlight  %}
The following screenshot displays the Right Button Style:

![F:/hdr.png](Customize-Right-Button_images/Customize-Right-Button_img2.png)



## RightButtonNavigationURL

This feature specifies the navigation URL of the page while clicking the right button.

{% highlight html %}
@Html.EJMobile().Header("header_sample").ShowRightButton(true).RightButtonNavigationUrl("")
{% endhighlight %}


