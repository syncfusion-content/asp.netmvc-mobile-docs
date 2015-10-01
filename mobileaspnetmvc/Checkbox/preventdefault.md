---
layout: post
title: Preventdefault | Checkbox | MobileAspNetMVC | Syncfusion
description: preventdefault 
platform: mobileaspnetmvc
control: Checkbox
documentation: ug
---

# PreventDefault 

In **CheckBox** control, the default actions are to Check or Uncheck the control. You can prevent this default action by setting this property to **true**. By default, this property is set to **false**.

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

@Html.EJMobile().CheckBox("apple").Text("Apple").**PreventDefault(true)**

</td>



<td width="100px">

@Html.EJMobile().CheckBox("android").Text("Android")

</td>

</tr>

<tr>

<td width="100px">

@Html.EJMobile().CheckBox("windows").Text("Windows")

</td>



<td width="100px">

@Html.EJMobile().CheckBox("Bberry").Text("BlackBerry")

</td>



</tr>

</table>

</div>

{% endhighlight %}

