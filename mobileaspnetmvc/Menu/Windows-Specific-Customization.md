---
layout: post
title: Windows Specific Customization| Menu | MobileAspNetMVC | Syncfusion
description: windows specific customization
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Windows Specific Customization

You can set the windows specific properties to the control by accessing Windows property.

## Type

When you click a button or target element, the Menu appears in contextual or popup mode. The appearance of the Menu is defined by Type property. 

The possible values are,

1. Contextual 
2. Popup

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.Windows)

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").RenderMode(RenderMode.Windows).Windows(windows=>windows.Type(WindowsMenuType.Contextual)).Items(item =>

{

item.Add().Text("Get info");

item.Add().Text("Show in folder");

item.Add().Text("Delete");

})

{% endhighlight %}

The following screenshot displays the Windows-specific Type:

![Type-Windows](Windows-Specific-Customization_images/Windows-Specific-Customization_img1.png)



