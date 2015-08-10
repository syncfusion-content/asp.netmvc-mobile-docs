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

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Single")                </td>

                <td width="100px">

                    @Html.EJMobile().RadioButton("sample_radiobutton", "").Text("Married")

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

The following screenshot displays **customized labels**:

{% include image.html url="customize-label_images/customize-label_img1.png" Caption="RadioButton-Text"%}

