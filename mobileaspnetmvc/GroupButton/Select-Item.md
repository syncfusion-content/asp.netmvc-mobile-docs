---
layout: post
title: Select Item| Group Button | MobileAspNetMVC | Syncfusion
description: select item
platform: mobileaspnetmvc
control: Group Button
documentation: ug
---

# Select Item

Group Button takes a numeric value given in the selectedItemIndex property and selects the corresponding item that matches the given index. Default value is 0.

{% highlight html %}

@Html.EJMobile().GroupButton("groupbutton_sample").GroupButtonType(GroupButtonType.radio).

SelectedItemIndex(1).Name("options").Buttons(button =>

{

button.Add().Text("ipad");

button.Add().Text("ipod");

button.Add().Text("iphone");

})

{% endhighlight %}

The following screenshot displays the Selected Item Index:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Groupbtton/images/android_1.png](Select-Item_images/Select-Item_img1.png)



