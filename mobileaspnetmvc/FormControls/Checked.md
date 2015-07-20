---
layout: post
title: Checked
description: checked 
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Checked 

This is a Boolean property that lets you choose whether RadioButton needs to be selected by default or not. By default, this property is set to false.



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



The following screenshot displays checked status:

{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML2022239a.PNG](Checked_images/Checked_img1.png)' | markdownify }}
{:.image }


