---
layout: post
title: enabled
description: enabled
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Enabled

The **Enabled** property that lets you enable or disable the options. When set to **false**, this prevents you from selecting that particular choice. By default, this property is set to **true**.



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

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Single")



                &lt;/td&gt;

                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married").**Enabled(false)**

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



The following screenshot displays **enabled** option:

{% include image.html url="enabled_images/enabled_img1.png" Caption="RadioButton-Enabled"%}

