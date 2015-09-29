---
layout: post
title: IOS7 Specific Customization| Menu | MobileAspNetMVC | Syncfusion
description: ios7 specific customization
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# IOS7 Specific Customization

You can set the iOS7 specific properties to the control by accessing iOS7 property.

## Cancel Button Customization

## Text and Color

The iOS7 Animate Type Menu comes with CancelButton at the bottom. The Cancel Button color can be customized by CancelButtonColor property. The Cancel Button text is changed by using CancelButtonText property. Set the desired text by using this property.

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.IOS7)

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").IOS7(ios7=>ios7.CancelButtonColor(IOS7ButtonColor.Red).CancelButtonText("Cancel")).Items(item =>

{

item.Add().Text("Get info");

item.Add().Text("Show in folder");

item.Add().Text("Delete");

})

{% endhighlight %}

The following screenshot displays the Button Customization:

![CancelButtonColor](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img1.png)



## Hide Cancel Button

You can hide or show the Cancel Button by setting false or true to the ShowCancelButton property.

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.IOS7)

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").IOS7(ios7=>ios7.ShowCancelButton(false)).Items(item =>

{

item.Add().Text("Get info");

item.Add().Text("Show in folder");

item.Add().Text("Delete");

})
			
{% endhighlight %}

The following screenshot displays the Show Cancel Button:

![ShowCancelButton](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img2.png)



## Title

When iOS7 Menu is used, it comes up with a Title on the top of the Menu container. You can hide or show the Title by setting false or true by using ShowTitle property. You can also change the Title text by setting the desired Title for Title property.

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.IOS7)

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").IOS7(ios7=>ios7.ShowTitle(false)).Items(item =>

{

item.Add().Text("Get info");

item.Add().Text("Show in folder");

item.Add().Text("Delete");

})

{% endhighlight %}

The following screenshot displays the Title:

![ShowTitle](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img3.png)



## Type

When you click a button or a target element, the Menu is shown. The appearance of the Menu is defined by the Type property. The possible values are,

1. Animate-This Menu is rendered in phone mode.
2.  Normal-This Menu is rendered in tablet mode.
3. Auto-This mode automatically updates the MenuType based on the mode of iOS7 device whether it is phone or tablet mode.

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu").RenderMode(RenderMode.IOS7)

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").IOS7(ios7=>ios7.Type(IOS7MenuType.Normal)).Items(item =>

{

item.Add().Text("Get info");

item.Add().Text("Show in folder");

item.Add().Text("Delete");

})

{% endhighlight %}

The following screenshot displays the Type:

![C:/Users/dineshr/Desktop/def.png](IOS7-Specific-Customization_images/IOS7-Specific-Customization_img4.png)



