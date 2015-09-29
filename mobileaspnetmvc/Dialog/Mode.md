---
layout: post
title: Mode| Dialog | MobileAspNetMVC | Syncfusion
description: mode
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Mode

The Mode property specifies the different types of dialog modes. The possible values are, 

1. Alert mode. 
2. Confirm mode.
3. Normal mode.
4. Full view mode.

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

{% highlight js %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img1.png)


## Confirm Mode

The ConfirmDialog box property is mostly used to take the user's consent on any option. It displays a Dialog box with two buttons, Ok and Cancel. Ok button returns true and Cancel button returns false.

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

{% highlight js %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img2.png)


## Normal Mode

The Normal Mode Dialog box property is used to display the message in sub screen area on a whole screen. It displays a Dialog box with two buttons, Continue and Cancel. Continue button returns true and Cancel button returns false. It is suitable for tablet devices.

{% tabs %}
{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome").Mode(DialogMode.Normal).Content(

@<div>

Syncfusion provides software components and tools for the Microsoft .NET platform.

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight js %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img3.png)


## Full View Mode

The FullViewDialog box property is used to display messages on full screen and it is suitable for mobile devices.

{% tabs %}
{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome").Mode(DialogMode.Fullview).Content(@<div>

Syncfusion provides software components and tools for the Microsoft .NET platform.

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight js %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Mode_images/Mode_img4.png)


