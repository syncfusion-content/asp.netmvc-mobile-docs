---
layout: post
title: Enable-and-Disable
description: enable and disable
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Enable and Disable

Enabled property is used to enable or disable your Textbox control. The default value is true.

Refer to the following code example.

    @Html.EJMobile().TextBox("textbox_sample").WatermarkText("Textbox").Enabled(false)

    @Html.EJMobile().PassWord("textbox_sample").WatermarkText("password").Enabled(false)

    @Html.EJMobile().TextArea("textbox_sample").WatermarkText("Textarea").Enabled(false)

    @Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("maskedit").Mask("+1 (999) 999-999").Enabled(false)



{ ![C:/Users/isuriyar/AppData/Local/Temp/SNAGHTML801ee361.PNG](Enable-and-Disable_images/Enable-and-Disable_img1.png) | markdownify }
{:.image }


