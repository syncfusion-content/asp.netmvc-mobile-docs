---
layout: post
title: Enabled | Checkbox | MobileAspNetMVC | Syncfusion
description: enabled 
platform: mobileaspnetmvc
control: Checkbox
documentation: ug
---

# Enabled 

This property enables you to **disable** or **enable** the control. By default, this property is set to **true**.

Refer to the following code examples.

{% highlight html %}

@Html.EJMobile().Header("sample_header").Title("CheckBox")

<div align="center" style="padding-top: 100px">

<div>

<b>Favorite Mobile</b>

</div>

<br />

<table border="0" cellpadding="6">

<tr>

<td width="100px">

@Html.EJMobile().CheckBox("apple").Text("Apple").**Enabled(false)**

</td>



<td width="100px">

@Html.EJMobile().CheckBox("android").Text("Android")**.Enabled(false)**



</td>

</tr>

<tr>

<td width="100px">

@Html.EJMobile().CheckBox("windows").Text("Windows").

</td>



<td width="100px">

@Html.EJMobile().CheckBox("Bberry").Text("BlackBerry")

</td>



</tr>

</table>

</div>

{% endhighlight %}

Execute the above code examples to render the following output.

{% include image.html url="enabled-_images/enabled-_img1.png" Caption="CheckBox with Enable and Disable state"%}

