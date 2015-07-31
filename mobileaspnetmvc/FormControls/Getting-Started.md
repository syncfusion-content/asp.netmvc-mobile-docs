---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Getting Started

In this section you can learn how to create FormControls in mobile app.

## Create your first Form in MVC

The ASP.NET MVC provides a way to create a Form with the following mobile widgets.

1. Textbox 
2. Numeric Textbox
3. Radiobutton 
4. Checkbox 
5. Button

From the following guidelines, you can create a BillPaymentApp where you can learn its features in the above mentioned widgets.

![](Getting-Started_images/Getting-Started_img1.png)

![](Getting-Started_images/Getting-Started_img2.png)



### Create the necessary layout 

In the BillPaymentApp, you can use the Textbox control to get the Name of the Person, Email, and Remarks, NumericTextbox control for the Amount field, Radio button for the Payment options, Check box for the terms and conditions, and Button control to submit the form.

Create a simple MVC application and add the following header and scrollpanel layout page content inside the <body> tag of layout.cshtml. 

1. Create an MVC Project and add necessary Dll’s and Scripts with help of the [MVC-Getting Started Documentation](http://help.syncfusion.com/ug/js/default.htm) for mobile.


~~~ html
     <!--Header Control-->

     @Html.EJMobile().Header("header").Title("Bill Payment")

      <div id="form_sample" class="sample">

         <div>

                @RenderBody()

          </div>

      </div>

      <!--Scroll Panel-->

      @Html.EJMobile().Scrollpanel("form_controls").Target("form_sample")
~~~
{:.pretty-print}





2. Add the following Layout code to the corresponding view page.

~~~ html
       <!--Add the Form Elements-->   

                <form id="form1">

                    <br />

                    <label>

                        Name of the Person:

                    </label>

                    <div>

                        <!--Add user name Text box Here-->



                    </div>

                    <br />

                    <label>

                        Amount:

                    </label>

                    <div>

                        <!--Add numeric text box for amount here-->



                    </div>

                    <br />

                    <div>

                        <label>

                            Payment Option:

                        </label>

                    </div>

                    <div>

                        <table class="radio">

                            <tr>

                                <td>

                                    <!--radio button for credit -->

                                </td>

                                <td>

                                    <!--radio button for debit-->



                                </td>

                            </tr>

                        </table>

                    </div>

                    <br />

                    <div>

                        <label>

                            Email:

                        </label>

                        <div>

                            <!--Add email text box here-->

                        </div>

                        <br />

                    </div>

                    <div>

                        <label>

                            Remarks (Optional):

                        </label>

                        <div>

                            <!--Add remark text box here-->

                        </div>

                        <br />

                    </div>

                    <div>

                        <table class="check">

                            <tr>

                                <td>

                                    <!--Add check box here-->



                                </td>

                            </tr>

                        </table>

                    </div>

                    <br />

                    <div align="center" class="submitbutton">

                        <!--Add submit button here-->



                    </div>

                </form>

 <!--Add Dialog Control for Payment Status-->

 @Html.EJMobile().Dialog("info_msg").Title("Alert").LeftButtonCaption("ok").EnableModal(true).EnableAutoOpen(false).Content(@<div id="dlgcontent"></div>).ClientSideEvents(evt => evt.ButtonTap("exit"))

~~~
{:.pretty-print}



3. Add the following styles.

~~~ css
      <style>

        .appview .submitbutton {

        text-align: center;

    }



    .appview .chksample {

        display: inline-block;

    }



    .appview #form_sample label.error {

        color: #FF0000;

    }



    .check td, .radio td {

        min-width: 150px;

    }



    .e-m-ios7 label, .e-m-ios7 .check, .e-m-ios7 .radio {

        padding-left: 10px;

    }



    .e-m-windows label, .e-m-windows .check {

        padding-left: 20px;

    }



    .e-m-windows .radio {

        padding-left: 20px;

    }



    .radio {

        padding-top: 5px;

    }



    .e-m-android #form_sample, .e-m-ios7 #form_sample {

        padding: 10px;

    }



    .e-m-android #form1 {

        padding: 0px 10px;

    }



    .e-m-windows #form_sample {

        padding: 3px;

    }      

</style>

~~~
{:.pretty-print}

### Add Textbox Control

TextboxControl is required to get the Name of the Person. To render this control, you can add the following Layout code to the corresponding view page.

{% highlight html %}
 <!—Textbox for Name of the Person-->

             @Html.EJMobile().TextBox("user_name")

                <label for="user_name" class="error" generated="true" />
{% endhighlight %}


Run the above code to render the following output. 

![](Getting-Started_images/Getting-Started_img3.png)



### Set Watermark text

The WatermarkText specifies a short hint that describes the expected value of the input field. This is achieved using the WatermarkText property. The following code example shows you how to set Watermarktext.

{% highlight html %}
      <!--Textbox-->

      @Html.EJMobile().TextBox("user_name").WatermarkText("Name")
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img4.png)



### Add Numeric Textbox Control

To render the NumericTextbox control, you can refer the following code example. 

{% highlight html %}
<!--Numeric Textbox-->

        @Html.EJMobile().NumericTextbox("amount").WatermarkText("Amount")

                <label for="amount" class="error" generated="true" />

{% endhighlight %}

![](Getting-Started_images/Getting-Started_img5.png)



### Disable Spin Button 

By default, the SpinButton is visible. Using this, you can increment or decrement the values. In the BillPaymentApp, SpinButton is not required. To hide this, you can set ShowSpinButton property to false.

{% highlight html %}
       <!--Numeric Textbox-->

       @Html.EJMobile().NumericTextbox("amt").WatermarkText("Amount")

       .ShowSpinButton(false)
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img6.png)



### Set Decimal Point 

By default, decimal numbers (floating point) are not allowed. In this case, you need to allow the decimal values since it is an amount field. To achieve this, you can set DecimalPlaces property with a numeric value that specifies the number of decimals allowed.

{% highlight html %}
        <!--Numeric Textbox-->

        @Html.EJMobile().NumericTextbox("amt").WatermarkText("Amount")

         .ShowSpinButton(false).DecimalPlaces(2)

{% endhighlight %}

### Add Radio Button Control

A RadioButton control is required for the payment option (credit or debit). By using Text property you can add the text for radio button. To render this control, add the following code example.

{% highlight html %}
       <!--Radio Button for Credit-->

@Html.EJMobile().RadioButton("radbtn", "credit", new { id = "credit" }).Text("Credit Card").Checked(true) 

       <!--Radio Button for Debit-->

@Html.EJMobile().RadioButton("radbtn", "debit", new { id = "debit" }).Text("Debit Card")

{% endhighlight %}

### Add Textbox for E-Mail

You can add Textbox for E-mail.

{% highlight html %}
<!--Textbox for E-mail-->

@Html.EJMobile().TextBox("mail").WatermarkText("user@mail.com")

<label for="mail" class="error" generated="true" />
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img7.png)



### Add Textbox for Remarks

You can add Textbox for Remarks.

{% highlight html %}
         <!--Textbox-->

 @Html.EJMobile().TextBox("remarks").WatermarkText("Remarks")
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img8.png)



### Add Checkbox Control

You can use Checkbox Control for “agree the terms and conditions” option. By using Text property, you can add the text to the checkbox control. To render this, add the following code example.

{% highlight html %}
    <!--Checkbox-->

@Html.EJMobile().CheckBox("chkbox").Text("I accept the terms and conditions")
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img9.png)



### Add Button Control

ButtonControl is required to submit the Form. By using client side events, you can perform form validation. Here TouchEnd event is used to perform the validation. To render this control, you need to add the following code example and also add the Text property to specify the Button text. 

{% highlight html %}
 <!--Button-->

@Html.EJMobile().Button("btn").Text("Pay Bill").ClientSideEvents(evt => evt.TouchEnd("formsubmit"))
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img10.png)



### Form Validation

You have created the Billpayment with required controls and for Validation you can use ASP.NET MVCMobileDialog control to show the Status of your payment.

{% highlight js %}
<script type="text/javascript">

    //$(function () {

    //    $("#btn").attr("name", "btn");

    //});

    function formsubmit(event) {

        validation();

        $("#form1").submit();

        $("#form_controls").ejmScrollPanel("refresh");

    }

    function exit() {

        var dialogObject = $("#info_msg").data("ejmDialog"); // creating instance for dialog

        dialogObject.close(); // close dialog

        $(".e-m-text-input").val("");

        $(".e-m-editor-input").val("");

        $("#chkbox").ejmCheckBox("model.checked", false);

    }



    function validation() {

        validator = $("#form1").validate({

            debug: true,

            rules: {

                user_name: { required: true },

                amount: { required: true, number: true },

                mail: { required: true, email: true }

            },

            messages: {

                user_name: { required: "Please enter user name" },

                amount: { required: "Please enter amount" },

                mail: { required: "Please enter e-mail" }

            },

            submitHandler: function (form) {

                var dialogObject = $("#info_msg").data("ejmDialog"); // creating instance for dialog

                if (!$("#chkbox").ejmCheckBox("isChecked")) {

                    dialogObject.open(); // open dialog

                    $("#dlgcontent").text("Could you please agree our terms and conditions ?");

                }

                else {

                    dialogObject.open();

                    $("#dlgcontent").text("Your payment is received successfully");

                }

            }

        });

    }

</script>
{% endhighlight %}




![](Getting-Started_images/Getting-Started_img11.png)

![](Getting-Started_images/Getting-Started_img12.png)



