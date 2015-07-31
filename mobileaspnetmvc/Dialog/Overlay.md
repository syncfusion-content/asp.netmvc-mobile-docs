---
layout: post
title: Overlay
description: overlay
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Overlay

The EnableModal property enables the modal Dialog that blocks you from interacting with the rest of the page until it is closed. The default value is false.


{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome to Syncfusion").LeftButtonCaption("Cancel").EnableModal(true).Content(

@<div>

Syncfusion provides software components and tools for the Microsoft .NET platform

</div>)

}



<div style="text-align: center">

@Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
{% endhighlight %}

{% highlight js%}
[Script]



        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}


The following screenshot displays the output.

![](Overlay_images/Overlay_img1.png)



