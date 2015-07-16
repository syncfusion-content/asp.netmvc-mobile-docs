---
layout: post
title: PreventDefault
description: preventdefault 
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# PreventDefault 

In CheckBox control, the default actions are to Check or Uncheck the control. You can prevent this default action by setting this property to true. By default, this property is set to false.

Refer to the following code examples.



@Html.EJMobile().Header("sample_header").Title("CheckBox")

&lt;div align="center" style="padding-top: 100px"&gt;

    &lt;div&gt;

        <b>Favorite Mobile</b>

    &lt;/div&gt;

    &lt;br /&gt;

    &lt;table border="0" cellpadding="6"&gt;

        &lt;tr&gt;

            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("apple").Text("Apple").PreventDefault(true)

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("android").Text("Android")

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("windows").Text("Windows")

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("Bberry").Text("BlackBerry")

            &lt;/td&gt;



        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



