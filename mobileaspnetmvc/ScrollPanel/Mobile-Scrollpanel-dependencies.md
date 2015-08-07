---
layout: post
title: Mobile-Scrollpanel-dependencies
description: mobile scrollpanel dependencies
platform: mobileaspnetmvc
control: ScrollPanel
documentation: ug
---

## Mobile Scrollpanel dependencies

This section deals with dependency files for ScrollPanel control. The file ej.mobile.all.min.js is a collection of Mobile Controls. When you are using this file, then you can skip this section. When not, then you need to refer to the following script files to render the ScrollPanel control.

_Script files_

<table>
<tr>
<td>
{{ '**File**' | markdownify }}</td><td>
{{ '**Description/Usage**' | markdownify }}</td></tr>
<tr>
<td>
ej.mobile.application.min.js</td><td>
It is referred to handle Mobile view port specifications.</td></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is referred always before using all the Mobile controls.</td></tr>
<tr>
<td>
ej.unobtrusive.min.js</td><td>
It is referred when the UnobtrusiveJavaScriptEnabled is set as true in web.config file.</td></tr>
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
ej.mobile.scrollbar.min.js</td><td>
It is referred for initializing scrollbars.</td></tr>
<tr>
<td>
ej.mobile.scrollpanel.min.js</td><td>
It is referred when using mobile ScrollPanel control.</td></tr>
</table>


