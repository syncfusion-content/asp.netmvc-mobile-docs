---
layout: post
title: Windows-specific-customization
description: windows specific customization
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Windows specific customization

You can set the Windows Specific properties to the control by accessing this property.

WindowsCustomText

In the Windows phones, by default, the Header title's text is in the lower case irrespective of whatever case is provided for the title. To disable this behavior, set the “windows.enablecustomtext”property to true. By default, the property value is set to false.

@Html.EJMobile().Header("header_sample").RenderMode(RenderMode.Windows).Windows(p => { p.EnableCustomText(true); }).Title("Custom Text")   

The following screenshot displays the Windows specific customization:

{ ![](Windows-specific-customization_images/Windows-specific-customization_img1.png) | markdownify }
{:.image }


