---
layout: post
title: Customize-Left-Button
description: customize left button
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Customize Left Button

## ShowLeftButton

In Footer control, you can view the previous page by using the ShowLeftButton. You can manually enable/disable the button by setting the true/false using ShowLeftButton property.

{% highlight html %}

@Html.EJMobile().Footer("footer_sample").ShowLeftButton(true)

{% endhighlight %}

The following screenshot displays the output.

![](Customize-Left-Button_images/Customize-Left-Button_img1.png)


## LeftButtonCaption 

To specify the caption (text) for Footer left button, set LeftButtonCaption property. 

{% highlight html %}

@Html.EJMobile().Footer("footer_sample").ShowLeftButton(true).LeftButtonCaption("Home")

{% endhighlight %}

The following screenshot displays the output.

![](Customize-Left-Button_images/Customize-Left-Button_img2.png)


## LeftButtonNavigationURL

Specifies the navigation URL to go to the page when the Left Button is clicked. 

{% highlight html %}

@Html.EJMobile().Footer("footer_sample").ShowLeftButton(true).LeftButtonNavigationUrl("")

{% endhighlight %}

