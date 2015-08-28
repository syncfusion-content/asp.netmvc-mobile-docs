---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Textbox
documentation: ug
---

# Getting Started

This section briefly describes how to create Essential MVC Mobile Textbox widget.

## Create your first Textbox Widget in MVC

To create a textbox for the login page in the mobile application, follow the guidelines given. 

![D:/Final Doc/mockup/IMG_0526_iphone5s_spacegrey_portrait.png](Getting-Started_images/Getting-Started_img1.png)





### Create the layout

Create an MVC application and add the following code example in the <body> tag of layout.cshtml file.

You can create a MVC project and add the necessary DLLs and scripts with the help of the [MVC Getting Started Documentation.](http://docs.syncfusion.com/js/)

{% highlight html %}

@Html.EJMobile().Header("header").Title("Login").Position(MobileHeaderPosition.Normal)

<div class="sample" style="padding:10px">

    <div class="frame">

        <div class="control">

            <table class="editors">

                <tbody>

                    <tr>

                        <td>

                            <label>

                                Name

                            </label>

                        </td>

                        <td>

                            <!--Add Textbox control-->

                        </td>

                    </tr>

                    <tr>

                        <td>

                            <label>

                                Password

                            </label>

                        </td>

                        <td>

                            <!--Password Control-->

                            @Html.EJMobile().PassWord("password").WatermarkText("Password")                           

                        </td>

                    </tr>

                </tbody>

            </table>

            <center>

                <div class="button">

                    <!--Button Control-->                    

                    @Html.EJMobile().Button("button").Text("Login")

                </div>

            </center>

        </div>

    </div>

</div>





{% endhighlight %}



### Add Textbox Control

To create the Textbox control, add the following code.

{% highlight html %}



@Html.EJMobile().TextBox("textbox_sample").WatermarkText("User Name")





{% endhighlight %}



Run the code and get the following output.

![D:/Final Doc/mockup/IMG_0531_iphone5s_spacegrey_portrait.png](Getting-Started_images/Getting-Started_img2.png)



