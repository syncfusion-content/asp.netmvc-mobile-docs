---
layout: post
title: Overlay| Dialog | MobileAspNetMVC | Syncfusion
description: overlay
platform: mobileaspnetmvc
control: Dialog
keywords: dialog
documentation: ug
---

# Overlay

The EnableModal property enables the modal Dialog that blocks you from interacting with the rest of the page until it is closed. The default value is false.

{% tabs %}
{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("London").LeftButtonCaption("Cancel").EnableModal(true).Content(

@<div>

 London, one of the most popular tourist destination in the world for a reason.

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight js%}



        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Overlay_images/Overlay_img1.png)



