---
layout: post
title: Type| Group Button | MobileAspNetMVC | Syncfusion
description: type
platform: mobileaspnetmvc
control: Group Button
documentation: ug
---

# Type

The Group Button is rendered via button and input tag elements. Group Button rendering is classified into three types: Button type, radio input type, and checkbox input type.

Option 1: Button 

{% highlight html %}

<!-- Group Button : button type -->

@Html.EJMobile().GroupButton("groupbutton_sample").Buttons(button =>

{

button.Add().Text("ipad");

button.Add().Text("ipod");

button.Add().Text("iphone");

})
	   
{% endhighlight %}

Option 2: Radio Button

{% highlight html %}

<!-- Group Button : radio type -->

@Html.EJMobile().GroupButton("groupbutton_sample").GroupButtonType(GroupButtonType.

radio).Name("options").Buttons(button =>

{

button.Add().Text("ipad");

button.Add().Text("ipod");

button.Add().Text("iphone");

})
	   
{% endhighlight %}

Option 3: Checkbox

{% highlight html %}

<!-- Group Button : checkbox type -->

@Html.EJMobile().GroupButton("groupbutton_sample").GroupButtonType(GroupButtonType.

checkbox).Name("options").Buttons(button =>

{

button.Add().Text("ipad");

button.Add().Text("ipod");

button.Add().Text("iphone");

})

{% endhighlight %}

The following screenshot displays the Group Button:

![](Type_images/Type_img1.png)




