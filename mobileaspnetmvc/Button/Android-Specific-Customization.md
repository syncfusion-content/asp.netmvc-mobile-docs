---
layout: post
title: Android Specific Customization| Button | MobileAspNetMVC | Syncfusion
description: android specific customization
platform: mobileaspnetmvc
control: Button
documentation: ug
---

# Android Specific Customization

You can set the **Android specific** properties to the control by accessing **Android** property****

## Style

You can change the style of Android mode button by setting **Style** property with **Android** specific. 

The possible values are

1. Normal

2. Small

3. Dialog

You can refer to the following code examples.

{% highlight html %}

 <div align="center" style="margin:10px">;

 @Html.EJMobile().Button("sample_button1").Text("Normal").RenderMode(RenderMode.Android).Android(e=>e.Style(AndroidButtonStyle.Normal)) 



@Html.EJMobile().Button("sample_button2").Text("Small").RenderMode(RenderMode.Android).Android(e=>e.Style(AndroidButtonStyle.Small))



@Html.EJMobile().Button("sample_button3").Text("Dialog").RenderMode(RenderMode.Android).Android(e=>e.Style(AndroidButtonStyle.Dialog))

</div>


{% endhighlight %}


{% include image.html url="Android-Specific-Customization_images/Android-Specific-Customization_img1.png" Caption="Button - Android Style"%}

