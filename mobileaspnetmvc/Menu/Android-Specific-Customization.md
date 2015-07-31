---
layout: post
title: Android-Specific-Customization
description: android specific customization
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

#Android Specific Customization

Set the Android Specific properties to the control by accessing “Android” property.

## Type

When you click a button or target element, the Menu appears in contextual or popup mode. The appearance of the Menu is defined by Type property. 

The possible values are, 

1. Contextual 
2. Popup
3. Optionmenu
4. Optionslist

{% highlight html %}

    <div style="text-align: center;">

        @Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.Android)

    </div>

    @Html.EJMobile().Menu("menu_sample").TargetId("menuitem").RenderMode(RenderMode.Android).Android(android=>android.Type(AndroidMenuType.Contextual)).Items(item =>

            {

                item.Add().Text("Get info");

                item.Add().Text("Show in folder");

                item.Add().Text("Delete");

            })
			
{% endhighlight %}

The following screenshot displays the Android-specific Type:

![Type-Android](Android-Specific-Customization_images/Android-Specific-Customization_img1.png)



