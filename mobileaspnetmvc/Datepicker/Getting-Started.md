---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: DatePicker
documentation: ug
---

# Getting Started

This section briefly describes how to create a DatePicker control in your application.

## Create your first DatePicker in MVC

The ASP.NET MVC DatePicker allows you to display the picker element in your webpage and allows you to pick the date. From the following guidelines, you can learn how to customize two DatePickers for a real-time ticket booking scenario. The following screenshot will demonstrate the functionality of DatePicker.



{ ![](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


Create a DatePicker 

ASP.NET MVC Mobile DatePicker widget can easily be created by using the MobileDatePicker Helper. To create an MVC Project and to add necessary Dlls and script, use the [MVC-Getting Started Documentation](http://help.syncfusion.com/ug/js/default.htm).

1. Add the following code example to the corresponding view page.

@Html.EJMobile().Header("header").Title("Ticket Booking")

&lt;div id="content_container"&gt;

    &lt;div&gt;

       &lt;!-- Add DatePicker Elements here --&gt;

    &lt;/div&gt;

&lt;/div&gt;





2. To render the DatePicker control, you can add the following code example, where two DatePickers are added, to specify start and end date.



    &lt;table&gt;

            &lt;tr&gt;

                <td class="tdclass">Onward Date</td>

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="tdclass"&gt;

                    &lt;span class="innerdp"&gt;

              &lt;!-- DatePicker control --&gt;

              @Html.EJMobile().DatePicker("startDate")

                    &lt;/span&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                <td class="tdclass">Return date</td>

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="tdclass"&gt;

                    &lt;span class="innerdp"&gt;

              &lt;!-- DatePicker control --&gt;

              @Html.EJMobile().DatePicker("endDate")

                    &lt;/span&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;



3. Apply the following styles to align the DatePickers.





    &lt;style type="text/css" class="cssStyles"&gt;

        .tdclass

        {

            width: 300px;

            font-weight: bold;

            padding-bottom: 10px;

        }



        table

        {

            margin: 30px auto;

        }

    &lt;/style&gt;



4. Run the above code example and you can see the following output.



{ ![](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


With the above mentioned steps, you can create two MobileDatePicker widgets in a page.

Set the Min and Max Date

In a real-time ticket booking scenario, the booking is open only for a limited number of days. You can select a date from that range. You can achieve this by using the properties minDate and maxDate. 



    &lt;script type="text/javascript"&gt;

        var curDate = new Date();// mentions the current date.

        // the below code mentions the 2 years from the current date.

        var rangeDate = new Date(curDate.getFullYear() + 2, curDate.getMonth(), curDate.getDate());



        // setting minDate and maxDate at the time of document ready.

        $(function () {

            var startdate = $("#startDate").data("ejmDatePicker");

            startdate.option({ "minDate": curDate, "maxDate": rangeDate });



            var enddate = $("#endDate").data("ejmDatePicker");

            enddate.option({ "minDate": curDate, "maxDate": rangeDate });

        });

    &lt;/script&gt;



Run the above code example to render the following output.

{ ![](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }


Set Event to Process Min and Max Date Validations

In the first DatePicker, after you select the Onward Journey Date, the Return Journey Date must be selected. This validation process is done after the selection of Onward Journey Date and the changes must be reflected on the Return Journey Date selection DatePicker. You can manipulate this process using the Select event of Onward Date Picker.

        &lt;table&gt;

            &lt;tr&gt;

                <td class="tdclass">Onward Date</td>

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="tdclass"&gt;

                    &lt;span class="innerdp"&gt;

              &lt;!-- DatePicker control --&gt;

              @Html.EJMobile().DatePicker("startDate").ClientSideEvents(eve => { eve.Select("selectedStartDate");})

                &lt;/span&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                <td class="tdclass">Return date</td>

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="tdclass"&gt;

                    &lt;span class="innerdp"&gt;

              &lt;!-- DatePicker control --&gt;

              @Html.EJMobile().DatePicker("endDate")

                    &lt;/span&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;    



By selecting the Onward Journey Date in the first DatePicker, you can select the Return Journey Date with the limited range. Add the following code example, to set the maxDate, to restrict false selection of date.



&lt;script type="text/javascript"&gt;

        function selectedStartDate(args) {

            var selDate = new Date(args.value); // mentions the selected date.

            minDatepicker = $("#endDate").data("ejmDatePicker");// creating DatePicker object

            minDatepicker.option({ "minDate": selDate });// setting minDate property through setModel of DatePicker object.

        }

&lt;/script&gt;    



Run the above code and you can see the following output.



{ ![](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }




By following the above mentioned steps, you can customize the MobileDatePicker widget in an efficient manner. You can also add additional functionalities to DatePicker like localization and date formats.



