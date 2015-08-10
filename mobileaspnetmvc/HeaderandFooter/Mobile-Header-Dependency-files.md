---
layout: post
title: Mobile-Header-Dependency-files
description: mobile header dependency files
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Mobile Header Dependency files

This section deals with the dependency files for the Header control. The file ej.mobile.all.min.js is a mass collection of Mobile Controls. When you are using this file, then you can skip this section. When you are not, you can refer to the following script files to render the Header control.

_Script Files_

<table>
<tr>
<th>
File                          </th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.mobile.application.min.js</td><td>
It is referred to handle the Mobile view port specifications.</td></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is always referred before using all the Mobile controls.</td></tr>
<tr>
<td>
ej.unobtrusive.min.js</td><td>
It is referred when the UnobtrusiveJavaScriptEnabled is set to true in the web.config file.</td></tr>
<tr>
<td>
ej.mobile.core.min.js</td><td>
It is referred to handle Mobile devices’ specifications.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
It is referred while using data binding feature in the Mobile controls that is used to handle data manager operation.</td></tr>
<tr>
<td>
ej.touch.min.js</td><td>
It is referred for touch events support.</td></tr>
<tr>
<td>
ej.mobile.header.min.js</td><td>
It is used to render the Header control that holds all the properties, events, and methods. It must be referred, otherwise the control is not created.</td></tr>
<tr>
<td>
ej.mobile.button.min.js</td><td>
This file should be used while enabling buttons on the Header.</td></tr>
</table>
