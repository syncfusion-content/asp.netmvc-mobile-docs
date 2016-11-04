---
layout: post
title: Templating| Dialog | MobileAspNetMVC | Syncfusion
description: templating                                  
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Templating                                  

The TemplateId property is used to define the ID of the template element where you can specify the content to render in the Dialog.

{% tabs %}
{% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("welcome").LeftButtonCaption("Cancel").TemplateId("temp").Content(

        @<div>

             London, one of the most popular tourist destinations in the world for a reason.

        </div>).Content(@<div id="temp">London</div>)

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


