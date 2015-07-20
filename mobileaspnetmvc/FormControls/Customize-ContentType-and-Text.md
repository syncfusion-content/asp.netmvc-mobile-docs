---
layout: post
title: Customize-ContentType-and-Text
description: customize contenttype and text
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Customize ContentType and Text

ContentType

You can make the Button appear as an image or text or combination of both. This property allows you to choose the ContentType of the Button in your application. By default, the ContentType of Button is set to ‘text’.

The possible values are

* Text
* Image
* Both

You can refer to the following code examples.

@Html.EJMobile().Button("sample_button").Text("button").ContentType(ButtonContentType.Text)



{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML1022c115.PNG](Customize-ContentType-and-Text_images/Customize-ContentType-and-Text_img1.png)' | markdownify }}
{:.image }


Text

This property allows you to specify the text to be appeared inside the Button using ‘Text’ property. 

You can refer to the following code examples.



           @Html.EJMobile().Button("sample_button").Text("button")





{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML1022c115.PNG](Customize-ContentType-and-Text_images/Customize-ContentType-and-Text_img2.png)' | markdownify }}
{:.image }


