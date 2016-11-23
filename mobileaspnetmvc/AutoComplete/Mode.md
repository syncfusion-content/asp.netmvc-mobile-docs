---
layout: post
title: Mode| AutoComplete  | MobileAspNetMVC | Syncfusion
description: mode
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
---

# Mode

Mode property specifies the textbox type. The possible values are,

1. Default
2. Search

Default is used to render the AutoComplete as normal textbox. Search is used to render the control with search icon. Default value for the property is “default”.


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields=>fields.Text("name")).Mode(Mode.Search)

{% endhighlight %}


The following screenshot displays Mode:

![](Mode_images/Mode_img1.png)


