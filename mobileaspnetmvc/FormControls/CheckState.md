---
layout: post
title: CheckState
description: checkstate
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# CheckState

This property enables you to specify the check state of the control by setting EnableTristate to “true”. By default, this property is set to true.

The possible values are:

1. Check
2. Uncheck
3. Indeterminate

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

                @Html.EJMobile().CheckBox("apple").Text("Apple").EnableTriState(true).CheckState(CheckState.Indeterminate)

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("android").Text("Android").EnableTriState(true).CheckState(CheckState.Check)

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("windows").Text("Windows").EnableTriState(true).CheckState(CheckState.Indeterminate)

            &lt;/td&gt;



            &lt;td width="100px"&gt;

                @Html.EJMobile().CheckBox("Bberry").Text("BlackBerry")

            &lt;/td&gt;



        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



Execute the above code examples to render the following output.

{ ![C:/Users/deepal/AppData/Local/Temp/SNAGHTML2f71445a.PNG](CheckState_images/CheckState_img1.png) | markdownify }
{:.image }


