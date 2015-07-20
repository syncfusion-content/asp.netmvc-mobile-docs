---
layout: post
title: Windows-specific-customization
description: windows specific customization
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Windows specific customization

The AllowReset property is used to reset the password value in windows rendermode. The default value is true.

Refer to the following code example.



@Html.EJMobile().PassWord("textbox_sample").WatermarkText("Password").RenderMode(RenderMode.Windows).Windows(windows=>windows.AllowReset(true))



{{ '![C:/Users/labuser/AppData/Local/Temp/SNAGHTMLa514ae.PNG](Windows-specific-customization_images/Windows-specific-customization_img1.png)' | markdownify }}
{:.image }


