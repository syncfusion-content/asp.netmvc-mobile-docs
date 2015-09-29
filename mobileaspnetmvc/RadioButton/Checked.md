---
layout: post
title: Checked | RadioButton | MobileAspNetMVC | Syncfusion
description: checked 
platform: mobileaspnetmvc
control: RadioButton
documentation: ug
---

# Checked 

This is a **Boolean** property that lets you choose whether **RadioButton** needs to be selected by default or not. By default, this property is set to **false**.

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

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Single").Checked(true)



</td>

<td width="100px">

@Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married ")

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

The following screenshot displays **checked** status:

{% include image.html url="Checked_images/Checked_img1.png" Caption="RadioButton-Checked"%}

