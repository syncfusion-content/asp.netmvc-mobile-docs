---
layout: post
title: readonly
description: readonly
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# ReadOnly

When it is set to true, you cannot edit the value in the **Textbox**. The default value is false.

Refer to the following code example.



    @Html.EJMobile().TextBox("textbox_sample"). WatermarkText("Textbox**").ReadOnly(true**)

    @Html.EJMobile().PassWord("textbox_sample"). WatermarkText ("password").**ReadOnly(true)**

    @Html.EJMobile().TextArea("textbox_sample").WatermarkText ("Textarea").**ReadOnly(true)**

    @Html.EJMobile().MaskEdit("textbox_sample").WatermarkText("maskedit").Mask("+1 (999) 999-9999").**ReadOnly(true)**



{% include image.html url="readonly_images/readonly_img1.png" Caption="Textbox -Read Only"%}

