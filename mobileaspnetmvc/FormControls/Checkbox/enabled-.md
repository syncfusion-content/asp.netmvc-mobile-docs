---
layout: post
title: enabled-
description: enabled 
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Enabled 

This property enables you to **disable** or **enable** the control. By default, this property is set to **true**.

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

                @Html.EJMobile().CheckBox("apple").Text("Apple").**Enabled(false)**

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("android").Text("Android")**.Enabled(false)**



            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("windows").Text("Windows").

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("Bberry").Text("BlackBerry")

            &lt;/td&gt;



        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



Execute the above code examples to render the following output.

{% include image.html url="enabled-_images/enabled-_img1.png" Caption="CheckBox with Enable and Disable state"%}

