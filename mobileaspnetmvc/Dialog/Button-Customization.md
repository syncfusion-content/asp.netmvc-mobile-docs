---
layout: post
title: Button Customization| Dialog | MobileAspNetMVC | Syncfusion
description: button customization
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Button Customization

## LeftButtonCaption

The LeftButtonCaption property is used to specify the text of the Left Button. The default value is cancel.


{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").LeftButtonCaption("Ok").EnableAutoOpen(true).Mode(DialogMode.Confirm).Content(

@<div>

Turn on cellular data or use Wi-Fi to access data

</div>)

}
{% endhighlight %}


The following screenshot displays the output.



![](Button-Customization_images/Button-Customization_img1.png)


## RightButtonCaption

The RightButtonCaption property specifies the text of the Right Button. The default value is continue.


{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").RightButtonCaption("Continue").EnableAutoOpen(true).Mode(DialogMode.Confirm).Content(

@<div>

Turn on cellular data or use Wi-Fi to access data

</div>)

}
{% endhighlight %}


The following screenshot displays the output.

![](Button-Customization_images/Button-Customization_img2.png)


## ShowButtons                                

The ShowButtons property is used to show the buttons in the Dialog box. The default value is true.


{% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("London").RightButtonCaption("Continue").EnableAutoOpen(true).ShowButtons(false).Mode(DialogMode.Confirm).Content(

        @<div>

             London, one of the most popular tourist destinations in the world for a reason.

        </div>)

}
{% endhighlight %}


The following screenshot displays the output.

![](Button-Customization_images/Button-Customization_img3.png)


