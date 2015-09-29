---
layout: post
title: enabled| Form Controls | MobileAspNetMVC | Syncfusion
description: enabled
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Enabled

The **Enabled** property that lets you enable or disable the options. When set to **false**, this prevents you from selecting that particular choice. By default, this property is set to **true**.

{% highlight html %}

<div align="center">

<br />

<div>

<div>

<div>

<b>Marital Status</b>

</div>

</div>

<br />

<table>

<tr>

<td width="100px">

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Single")



</td>

<td width="100px">

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married").Enabled(false)

</td>

</tr>

<tr>

<td width="100px">

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Divorced")

</td>



<td width="100px">

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Widowed")

</td>	



</tr>

</table>

</div>

</div>

{% endhighlight %}

The following screenshot displays **enabled** option:

{% include image.html url="Enabled_images/Enabled_img1.png" Caption="RadioButton-Enabled"%}

