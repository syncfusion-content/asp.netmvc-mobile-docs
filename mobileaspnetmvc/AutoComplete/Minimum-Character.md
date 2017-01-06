---
layout: post
title: Minimum Character| AutoComplete  | MobileAspNetMVC | Syncfusion
description: minimum character
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
---

# MinimumCharacter

Minimum Character specifies the minimum number of characters you can enter in the text box to display the suggestion list. By default the value is set to “1”.


{% highlight html %}
@model List<Cars>

  @Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select a car").DataSource(Model).Fields(field => field.Text("country")).MinimumCharacter(2)
{% endhighlight %}


