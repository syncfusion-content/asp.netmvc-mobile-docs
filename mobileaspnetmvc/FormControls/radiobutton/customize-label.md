---
layout: post
title: customize-label
description: customize label
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Customize Label

The **Text** property lets you set labels for the **RadioButton**. To set the text for the **RadioButton,** you can refer the following code example.



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

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").**Text("Single")**                &lt;/td&gt;

                &lt;td width="100px"&gt;

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married")

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



The following screenshot displays **customized labels**:

{% include image.html url="customize-label_images/customize-label_img1.png" Caption="RadioButton-Text"%}

