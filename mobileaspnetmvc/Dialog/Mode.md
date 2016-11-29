---
layout: post
title: Mode| Dialog | MobileAspNetMVC | Syncfusion
description: mode
platform: mobileaspnetmvc
control: Dialog
keywords: dialog, mode
documentation: ug
---

# Mode

The Mode property specifies the different types of dialog modes. The possible values are, 

1. Alert mode. 
2. Confirm mode.
3. Custom mode.


## Alert Mode


The AlertDialog box property is used to communicate an Alert message.

{% tabs %}
{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Mode(DialogMode.Alert).Content(

@<div>

5% of battery remaining

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight javascript %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img1.png)


## Confirm Mode

The ConfirmDialog box property is mostly used to take the user's content on any option. It displays a Dialog box with two buttons, Ok and Cancel. Ok button returns true and Cancel button returns false.

{% tabs %}
{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").Mode(DialogMode.Confirm).Content(

@<div>

Turn on cellular data or use Wi-Fi to access data

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight javascript %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img2.png)


## Custom Mode

The custom'Mode' Dialog box property  displays the dialog as custom type.

{% tabs %}
{% highlight html %}

            @{

                @Html.EJMobile().Dialog("alertdlg").Title("Welcome").Mode(DialogMode.Custom).Content(

                    @<div>

                         London, one of the most popular tourist destination in the world for a reason.

                    </div>)

            }



            <div style="text-align: center">

                @Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

            </div>

{% endhighlight %}

{% highlight javascript %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img3.png)



