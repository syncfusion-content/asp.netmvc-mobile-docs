---
layout: post
title: Multi Selection| AutoComplete  | MobileAspNetMVC | Syncfusion
description: multi selection
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
---

# Multi selection

This feature is enabled by setting the “EnableMultiSelect” property to true.

## DelimiterChar

DelimiterChar is used to separate two or more items in the AutoComplete textbox. When you set DelimiterChar property then the value gets accepted in the textbox only after the delimiter character. Default value is “,”.

You can refer to the following code examples.


{% highlight html %}
@model List<Cars>

        @Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select a car").DataSource(Model).Fields(fields=>fields.Text("name")).EnableMultiSelect(true).DelimiterChar(";")
{% endhighlight %}


The following screenshot displays the DelimiterChar:

![](multi-selection_images\multi-value-selection_img1.png)




