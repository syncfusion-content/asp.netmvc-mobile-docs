---
layout: post
title: Mobile-RadioButton-dependency-files
description: mobile radiobutton dependency files
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Mobile RadioButton dependency files

This section deals with the dependency files for RadioButton control. The file ej.mobile.all.min.js is a collection of Mobile Controls. If you are using this file, then you can skip this section. If not, then you need to refer to the following script files to render the RadioButton control.

_Script files_

<table>
<tr>
<td>
{{ '*File*' | markdownify }}</td><td>
{{ '*Description/Usage*' | markdownify }}</td></tr>
<tr>
<td>
ej.mobile.application.min.js</td><td>
It is referred to handle Mobile view port specifications.</td></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is always referred before using all the Mobile controls.</td></tr>
<tr>
<td>
ej.unobtrusive.min.js</td><td>
It is referred when the UnobtrusiveJavaScriptEnabled is set to true in web.config file.</td></tr>
<tr>
<td>
ej.mobile.core.min.js</td><td>
It is referred to handle Mobile device specifications.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
It is referred while using data binding feature in Mobile controls that is used to handle data manager operation.</td></tr>
<tr>
<td>
ej.touch.min.js</td><td>
It is referred for touch events support.</td></tr>
<tr>
<td>
ej.mobile.radiobutton.min.js</td><td>
It is used to render the radiobutton control that holds all the properties, events, and methods. It must be referred, otherwise the control is not created.</td></tr>
</table>


