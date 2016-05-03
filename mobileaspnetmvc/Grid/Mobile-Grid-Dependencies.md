---
layout: post
title: Mobile Grid Dependencies| Grid | MobileAspNetMVC | Syncfusion
description: mobile grid dependencies
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Mobile Grid Dependencies

ej.mobile.all.js is a bundle of all ASP.NET MVC mobile controls. When you are using ej.mobile.all.js in your application, then you can leave this section or else you tried to render ejmgrid in your application using ej.mobile.grid file then need to refer following frameworks and controls in your project.

ASP.NET MVC mobile controls table

<table>
<tr>
<th>
File</th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js</td><td>
Must be referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.mobile.application.min.js </td><td>
Must be referred always before using all the Mobile JS controls. To create pages for different resolution mobile devices.</td></tr>
<tr>
<td>
ej.mobile.core.min.js</td><td>
Must be referred always before using all the Mobile JS controls.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle datamanger operation and should be used while binding data to JS controls.</td></tr>
<tr>
<td>
ej.mobile.grid.min.js</td><td>
Should be referred when using grid control.</td></tr>
<tr>
<td>
ej.mobile.button.min.js</td><td rowspan = "4">
<br>These files should be referred to achieve different grid features.</td></tr>
<tr>
<td>
ej.mobile.dialog.min.js</td></tr>
<tr>
<td>
ej.mobile.header.min.js</td></tr>
<tr>
<td>
ej.mobile.listbox.min.js</td></tr>
<tr>
<td>
ej.mobile.scrollpanel.min.js</td><td>
Should be referred when using scrolling is enabled in grid.  </td></tr>
</table>

