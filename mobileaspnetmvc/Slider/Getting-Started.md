---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Slider
documentation: ug
---

# Getting Started

This section briefly describes how to create and use a Slider in your application.

## Create your first Slider in MVC

The ASP.NET MVC Mobile Slider allows you to select a single value or a range of values using an interface with sliding handles.  The following section describes how to create a shopping cart app and learn the features in Slider widget.



{{ '![1](Getting-Started_images/Getting-Started_img1.png)' | markdownify }}
{:.image }


Create the layout for Shopping cart app	 

You can customize Slider control by changing their properties. In shopping cart app a range slider is used to set price range.

Create a simple MVC application and add the following code example in the <body> tag of Layout.cshtml file.

You can create a MVC project and add necessary DLL’s and scripts with the help of the [MVC Getting Started Documentation.](http://help.syncfusion.com/ug/js/default.htm)

@Html.EJMobile().Header("header").Title("Shopping cart")



    <div id="content">



        <div>



            @RenderBody()



        </div>



    </div>



       @Html.EJMobile().Scrollpanel("scroll").Target("content")



Add the following code example to the corresponding view page.

<div id="form" style="margin: 20px;">

     <div style="margin-bottom: 10px">

         <div style="margin-top:10px;">

             <h1>Search-->MobilePhones-->Filter</h1>

          </div>

           <h1>Operating System</h1>

      </div>

       <!-- create check box for different OS  -->

       <div align="center" id="checkbox" style="margin-bottom:10px">

       <table border="0" cellpadding="6">

        <tr>

         @Html.EJMobile().CheckBox("check1").Text("IOS7")

        </tr>

        <tr>

          @Html.EJMobile().CheckBox("check3").Text("Android")

        </tr>

        <tr>

          @Html.EJMobile().CheckBox("check2").Text("Windows")

        </tr>

       </table>

           </div>

           <div style="margin-bottom: 10px">

               <h1>Price Range</h1>

            </div>

            <b>Min:</b><span id="min">      <b>Max:  </b></span><span id="max" style="float:right"></span>

             <!—Add your Slider control here-->

             </div>

             <div align=center style="margin-top:20px;">

            @Html.EJMobile().Button("submit").Text("SUBMIT").ClientSideEvents(events => events.TouchEnd("openAlertDialog"))

              </div>

              <!-- dialog control -->

   @Html.EJMobile().Dialog("alert").LeftButtonCaption("OK").ClientSideEvents(events r=> events.ButtonTap("alertClose")).Content(@<div>

      Based on your suggestions the phones will display now

               </div>).EnableAutoOpen(false)



Execute the above code to render the following output. 

{{ '![2](Getting-Started_images/Getting-Started_img2.png)' | markdownify }}
{:.image }


Create the Slider control

To create the Slider control with a predefined range, add the following code to the view page. In this application you can set the minimum value for the Slider using MinimumValue property as 100, maximum valueusing MaximumValue property as 5000 and the value of IncrementStep property to 100 so that, the slider is moved for every 100 values. 

@Html.EJMobile().Slider("slider1").MinimumValue(100).MaximumValue(5000).IncrementStep(100)

{{ '![3](Getting-Started_images/Getting-Started_img3.png)' | markdownify }}
{:.image }


Create the range slider

In this scenario, you can set EnableRange property to True to set the price range using range slider. You can set the initial range values using Values property as 100, 1500. And set the Slider’s left thumb to 100 and the right thumb to 1500. 

Add the following code to the Slider<div> tag.



@Html.EJMobile().Slider("slider").MinimumValue(100).MaximumValue(5000).EnableRange(true).IncrementStep(100).Values(new int[] { 100, 1500 })



Execute the above code to render the following output. 

{{ '![4](Getting-Started_images/Getting-Started_img4.png)' | markdownify }}
{:.image }


Handle slider events

In this shopping cart app, when you move the slider, the corresponding values are updated to the span elements that act as a label for Slider. You can use “Slide” event that is handled by appropriate function. 

Add the following code example to the Slider.



@Html.EJMobile().Slider("slider").MinimumValue(100).MaximumValue(5000).EnableRange(true).IncrementStep(100).Values(new int[] { 100, 1500 }).ClientSideEvents(events => { events.Slide("onSlide"); })





You can get the present value of both the Slider handles at any time using its getValue property.  Add the following code example to the <script> tag.



//to display the slider value in span element (label) at initialize

    $(function (args) {

        window.dialogObject = $("#alert").data("ejmDialog"); //to create dialog object

        window.sliderObject = $("#slider").data("ejmSlider"); //to create slider object

        setValue("300,1500");//set slider labels at initialize

    });

    // handling slider slide event

    function onSlide() {

        var value = window.sliderObject.getValue();// get the value of slider by using getValue API

        setValue(value);

    }

    function setValue(value) {

        var position = value.indexOf(",");

        var min = value.substring(0, position); //to get left thumb value

        var max = value.substring(position + 1); //to get right thumb value

        $("#min").html("$" + min); //to set left thumb value to the left span

        $("#max").html("$" + max); // to set right thumb value to the right span

    }



Execute the above code to render the following output. 

{{ '![5](Getting-Started_images/Getting-Started_img5.png)' | markdownify }}
{:.image }


Add extra functionalities to Shopping cart

In the shopping cart app, a dialog displays to provide the information about the search when you click submit. Add the following code example to display the dialog.



<script>

function alertClose() {



        $("#alertdlg").ejmDialog("close");



    }      //to open dialog add this code inside the script tag



         function openAlertDialog(args) {



        App.activePage.find("#alertdlg").ejmDialog("open");



    }//close dialog

</script>





Execute the above code to render the following output, when you click submit. 



{{ '![6](Getting-Started_images/Getting-Started_img6.png)' | markdownify }}
{:.image }


