---
layout: post
title: Hide-Footer
description: hide footer
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Hide Footer

In some cases (for example, when toolbar is used in the application), Footer control need not be displayed in Android and Windows Platforms. For this scenario, you can use hideforunsupporteddevice property. When this property is set to true, Footer is visible for IOS7rendermode alone and is not visible in Android and Windows rendermode. By default, the property value is set to false.

@Html.EJMobile().Footer("footer_sample").HideForUnSupportedDevice(true)



