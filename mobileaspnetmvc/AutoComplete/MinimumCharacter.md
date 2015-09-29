---
layout: post
title: MinimumCharacter| AutoComplete  | MobileAspNetMVC | Syncfusion
description: minimumcharacter
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
---

# MinimumCharacter

MinimumCharacter specifies the minimum number of characters you can enter in the text box to display the suggestion list. By default the value is set to “1”.


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select a car").DataSource(Model).Field("name").MinimumCharacter(2)
{% endhighlight %}


