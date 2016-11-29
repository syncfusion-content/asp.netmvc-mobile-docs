---
layout: post
title: Templating| Dialog | MobileAspNetMVC | Syncfusion
description: templating                                  
platform: mobileaspnetmvc
control: Dialog
keywords: dialog, templating
documentation: ug
---

# Templating                                  

To define the ID of the template element where you can specify the content to render in the Dialog.

{% tabs %}
{% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("Welcome").LeftButtonCaption("Cancel").TemplateId("temp").Content(

    @<div>

  </div>).Content(@<div id="temp">London, one of the most popular tourist destination in the world for a reason.</div>)

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

![](Templating_images/Templating_img1.png)


