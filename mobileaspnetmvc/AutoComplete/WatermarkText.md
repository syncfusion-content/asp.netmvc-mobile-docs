---
layout: post
title: WatermarkText| AutoComplete  | MobileAspNetMVC | Syncfusion
description: watermarktext
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
kewords : watermarktext
---

# Watermarktext

WatermarkText property displays text in the AutoComplete textbox when it is empty. It acts like a label for the textbox. When you enter the query, the WatermarkText disappears and the typed text is entered in the textbox. Default value for the property is set to “search”.


{% highlight html %}
@model List<Cars>

        @Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select a car").DataSource(Model).Fields(fields => fields.Text("name")).WatermarkText("Search a Car")
{% endhighlight %}



The following screenshot displays Watermark text:

![](WatermarkText_images\customize-watermarktext_img1.png)




