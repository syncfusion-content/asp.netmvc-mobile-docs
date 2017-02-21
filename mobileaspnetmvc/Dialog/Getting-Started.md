---
layout: post
title: Getting Started| Dialog | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Dialog
keywords: dialog, model
documentation: ug
---

# Getting Started

This section explains briefly on how to create a Dialog control in your application.

## Create your first Dialog in MVC

The ASP.NET MVCDialog window is an overlay positioned within the AppView and displays a message along with supplementary content such as images or text and interactive content such as forms etc. It contains a title and a content area. The following example explains how to create a MailSign in form through that you can learn the features of the ASP.NET MVC Dialog widget.

![](Getting-Started_images/Getting-Started_img1.png)



Alert Dialog
{:.caption}  

### Create the required layout

You can render the Dialog control based on the default values for all the properties. You can easily customize Dialog control by changing its properties according to your requirement. Create a simple MVC application and add the following header and scrollpanel layout page content inside the <body> tag of layout.cshtml. For creating a MVC Project, adding necessary Dll’s and Scripts can be done with help of the [MVC-Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started) for mobile. 

{% highlight html %}
<!-- header control -->          

@Html.EJMobile().NavigationBar("header").Title("Mail")

<div id="content">

    <div>

        @*Render Dialog control*@

    </div>

</div>

<!-- ScrollPanel -->
@Html.EJMobile().Scrollpanel("scroll").Target("content")
{% endhighlight %}


Add the following Layout code to the corresponding view page
{% highlight html%}
<div id="content">

    <div>

        @*Render Dialog control*@

        <div id="content">

            <div>

                <!-- Adding Mail Sign in Form -->



                <form id="form1">



                    <label>

                        Name:



                    </label>



                    <div>

                        @Html.EJMobile().TextBox("name_def").WatermarkText("Name")

                        <label for="name_def" class="error" generated="true" />



                    </div>



                    <label>

                        Email:



                    </label>



                    <div>

                        @Html.EJMobile().TextBox("email_def").WatermarkText("user@mail.com")

                        <label for="email_def" class="error" generated="true" />



                    </div>



                    <label>

                        Password:



                    </label>



                    <div>

                        @Html.EJMobile().PassWord("password_def").WatermarkText("Required")

                        <label for="password_def" class="error" generated="true" />

                    </div>



                    <label>

                        Job Description (Optional):



                    </label>



                    <div>



                        @Html.EJMobile().TextBox("description_def")



                    </div>
                    <center>
                        @Html.EJMobile().Button("button").Text("Save").ClientSideEvents(eve => eve.TouchEnd("formsubmit"))
                    </center>


                </form>

                @Html.EJMobile().Dialog("alertdlg").Title("Success").LeftButtonCaption("OK").Content(@<div id="contentDialog"></div>)

            </div>

            </div>

        </div>



        <!-- Adding Dialog Helper Here -->



{% endhighlight %}


Use the following styles for adding content element.
{% highlight css%}
<style type="text/css">

    .appview.e-m-ios7 #content {

        background: #dddddd;

        padding: 10px;

    }



    #form > div {

        padding: 10px 0;

    }



    .appview #form1 label.error {

        color: Red;

    }



    .e-m-ios7 label {

        padding-left: 10px;

    }



    .e-m-windows label {

        padding-left: 20px;

    }



    .e-m-android #content, .e-m-ios7 #content {

        padding: 10px;

    }



    .e-m-android #form1 {

        padding: 0px 10px;

    }



    .e-m-windows #content {

        padding: 3px;

    }

</style>
{% endhighlight %}


Execute this code to render the following output. For more details, to run the sample refers "Common Getting Started" section.

![](Getting-Started_images/Getting-Started_img2.png)



Mail Sign in Form
{:.caption}

## Create the Dialog control

There are four types of Dialog modes namely alert, confirm, normal and full view Dialogs. The defaultDialog mode is “alert”. In your use case, an error message is displayed when invalid details are entered. AlertDialog contains title, content and a button. 

To render the Dialog control, you can add the following code example and specify the Dialog content (HTML content) using “Content” API. Specify a value for “Title” property to set title for Dialog. In your case you can set it as “Invalid email address”. Specify a value for “LeftButtonCaption” property to set Dialog button text; here you can set it as “OK”. 

 {% highlight html%}
       @Html.EJMobile().Dialog("alertdlg").Title("Success").LeftButtonCaption("OK").Content(@<div id="contentDialog"></div>)

    </div>

</div>

{% endhighlight %}

## Display the Dialog

To display the Dialog, you can click the save button. The click event is handled by “formsubmit” function as mentioned as follows. Create an object for Dialog control and then using the dialog’s “open” function you can display the Dialog. 

Add the following script code to the <body> tag.
{% highlight js%}
<script type="text/javascript">

        function formsubmit(event) {

            validation();

            $("#form1").submit();

            $("#ScrollPanel").ejmScrollPanel("refresh");

        }

        function validation() {

            validator = $("#form1").validate({

                messages: {

                    name_def: { required: "Please enter user name" },

                    password_def: { required: "Please enter password" },

                    email_def: { required: "Please enter e-mail" }

                },

                submitHandler: function (form) {

                    var dialogObject = $("#alertdlg").data("ejmDialog"); // creating instance for dialog

                    dialogObject.open();

                    $("#contentDialog").text("Your details are saved successfully");

                }

            });

        }

</script>
{% endhighlight %}


Execute this code to render the following output. For more details, to run the sample refers "Common Getting Started" section.

![](Getting-Started_images/Getting-Started_img3.png)



## Enable Modal Dialog

The EnableModalDialog prevents you from interacting with the rest of the page until it is closed. Enable the modal Dialog using “EnableModal” property.
{% highlight html%}
        @Html.EJMobile().Dialog("alertdlg").Title("Success").LeftButtonCaption("OK").Content(@<div id="contentDialog"></div>).EnableModal(true)

    </div>

</div>

{% endhighlight %}

Execute this code to render the following output. For more details, to run the sample refers "Common Getting Started" section.

![](Getting-Started_images/Getting-Started_img4.png)


