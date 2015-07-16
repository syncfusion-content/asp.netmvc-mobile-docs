---
layout: post
title: Hide-Header
description: hide header
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Hide Header

In some cases (for example, when tab is used in the application), Header control need not be displayed in Android and Windows Platforms. For this scenario, set “hideforunsupporteddevice” property. When this property is set to true, Header is visible for iOS7rendermode alone and not visible in Android and Windows rendermode. By default, the property value is set to false.

@Html.EJMobile().Header("header_sample").HideForUnSupportedDevice(true)



