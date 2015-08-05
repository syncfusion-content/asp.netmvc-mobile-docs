---
layout: post
title: checked-
description: checked 
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Checked 

This is a **Boolean** property that lets you choose whether **RadioButton** needs to be selected by default or not. By default, this property is set to **false**.



&lt;div align="center"&gt;

    &lt;br /&gt;

    &lt;div&gt;

        &lt;div&gt;

            &lt;div&gt;

                <b>Marital Status</b>

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;br /&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Single").**Checked(true)**



                &lt;/td&gt;

                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married ")

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Divorced")

                &lt;/td&gt;



                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Widowed")

                &lt;/td&gt;



            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;

&lt;/div&gt;



The following screenshot displays **checked** status:

{% include image.html url="checked-_images/checked-_img1.png" Caption="RadioButton-Checked"%}

