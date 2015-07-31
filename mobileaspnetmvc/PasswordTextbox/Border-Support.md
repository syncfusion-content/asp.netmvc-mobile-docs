---
layout: post
title: Border-Support
description: border support
platform: mobileaspnetmvc
control: Password
documentation: ug
---

## Border Support

The ShowBorder property is used to decide whether the Password border can be visible or hidden. The default value is “True”.

Refer to the following code example.

{% highlight html %}



    @Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").ShowBorder(false)


{% endhighlight %}



