---
layout: post
title: Title| Dialog | MobileAspNetMVC | Syncfusion
description: title
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Title

The Title property is used to display the title text of the Dialog box. 

{% tabs %}
{% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("Welcome").LeftButtonCaption("Cancel").Content(

        @<div>

             London, one of the most popular tourist destinations in the world for a reason.

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

![](Title_images/Title_img1.png)



