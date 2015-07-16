---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: TimePicker
documentation: ug
---

# Getting Started

This section briefly describes you on how to create the Essential Studio for ASP.NET MVC, Mobile TimePicker control in your application.

## Create your first TimePicker in MVC

The ASP.NET MVC TimePicker provides support to display the TimePicker element within your web page and allows you to pick the time. From the following guidelines, you can learn how to customize two TimePickers for a real time hotel reservation scenario. The following screenshot demonstrates the functionality of TimePicker.



{ ![](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


Create the necessary layout

You can create ASP.NET MVCTimePicker widget easily by using MobileTimepickerHTML helper.

Create a simple MVC application and add the following header content inside the <Body>tag of layout.cshtml. You can create a MVC Project and add necessary Dlls and scripts using [MVC-Getting Started Documentation.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)



@Html.EJMobile().Header("header").Title("Hotel Reservation").Position(MobileHeaderPosition.Normal)

   &lt;div&gt;

@RenderBody()

  &lt;/div&gt;



Add the following code example to the corresponding view page. Here you can add two TimePickers to specify InTime and OutTime.

       &lt;div align="center"&gt;

 &lt;table&gt;

             &lt;tr&gt;

                <td class="tdclass">Date</td>

                &lt;td class="innerclass"&gt;

                    &lt;span class="innerdp"&gt;

               &lt;!-- Creating DatePicker to select the booking date --&gt;

                 @Html.EJMobile().DatePicker("entryDate")").Value("01/01/2000")



                    &lt;/span&gt;

                &lt;/td&gt;

             &lt;/tr&gt;

             &lt;tr&gt;

                <td class="tdclass">In Time</td>

                &lt;td class="innerclass"&gt;

                    &lt;span class="innerdp"&gt;

                &lt;!-- Add InTime Timepicker control here --&gt;

                    &lt;/span&gt;

                &lt;/td&gt;

             &lt;/tr&gt;

             &lt;tr&gt;

                <td class="tdclass">Out Time &lt;/td&gt;

                &lt;td class="innerclass"&gt;

                    &lt;span class="innerdp"&gt;

                &lt;!-- Add OutTime Timepicker control here --&gt;

                    &lt;/span&gt;

                &lt;/td&gt;

             &lt;/tr&gt;

        &lt;/table&gt;



           &lt;div&gt;

               &lt;!-- Creating button to reserve the hotel --&gt;

                @Html.EJMobile().Button("button").Text("Book Now").RenderMode(RenderMode.Auto).ClientSideEvents(evt=>evt.TouchEnd("displayConfirmation"))

          &lt;/div&gt;                                                                        &lt;/div&gt; 





Run the above code to render the following output.

{ ![](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


Create a TimePicker

To render the TimePicker control, you can add the following code example. Here two TimePickers are added to specify InTime and OutTime.



  &lt;!-- InTime Timepicker element --&gt;

      @Html.EJMobile().TimePicker("startTime").HourMode(HourFormat.TwentyFour).Value("11:00")

  &lt;!-- OutTime Timepicker element --&gt;

      @Html.EJMobile().TimePicker("endTime").HourMode(HourFormat.TwentyFour).Value("21:00")





Apply the following styles to align the MVCMobileTimePicker.

<table>
<tr>
<td>
     &lt;style type="text/css" class="cssStyles"&gt;        .tdclass {            width: 100px;                        }        Table   {            margin: 10px;                }.innerclass {            width: 300px;             padding: 10px;                     }     &lt;/style&gt;</td></tr>
<tr>
<td>
</td></tr>
</table>


Run the above code and focus on InTime or OutTimeTimePicker element (here OutTime element is focused) to render the following output.

{ ![](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }


Set the Hour Format

The TimePicker widget supports both 12 hour and 24 hour time format. The default value is 24 hour format. In this case, the booking table opens for all time throughout the day. You can refer the following code example to set 24 hour format using “HourFormat” property and add it to corresponding view page.



  &lt;!-- InTime Timepicker element --&gt;

       @Html.EJMobile().TimePicker("startTime").HourMode(HourFormat.TwentyFour)

  &lt;!-- OutTime Timepicker element --&gt;

       @Html.EJMobile().TimePicker("endTime").HourMode(HourFormat.TwentyFour)





Run this code and focus on InTime or OutTimeTimePicker element (here OutTime element is focused) to render the following output.

{ ![](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }


Refer the following code example to display a confirmation message by clicking the Book button handled by the button touch and event. 



@Html.EJMobile().Dialog("alertdlg").Title("Booking Confirmation").Mode(DialogMode.Alert).LeftButtonCaption("OK").EnableModal(true).EnableAutoOpen(false).Content(@<div>Hotel reserved for specified time</div>).ClientSideEvents(evt => { evt.ButtonTap("alertClose"); })



&lt;script&gt;

    function alertClose() {

        $("#alertdlg").ejmDialog("close");    //to close dialog

    }

    function displayConfirmation(args) {

        App.activePage.find("#alertdlg").ejmDialog("open");  //to open dialog

    }



&lt;/script&gt;

Run the above code and click Book Now button to render the confirmation message as displayed in the following screenshot.



{ ![](Getting-Started_images/Getting-Started_img5.png) | markdownify }
{:.image }


You can also add additional functionalities to TimePicker like time formats.

