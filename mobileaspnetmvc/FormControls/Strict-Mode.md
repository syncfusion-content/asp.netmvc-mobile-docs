---
layout: post
title: Strict-Mode
description: strict mode
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Strict Mode

EnableStrictMode property makes Textbox accept only a value between the defined maximum and minimum values when it is set to true.



@Html.EJMobile().NumericTextbox("textbox_sample").MinimumValue(30).MaximumValue(100).EnableStrictMode(true)



The following screenshot displays the output.

{ ![](Strict-Mode_images/Strict-Mode_img1.png) | markdownify }
{:.image }


