---
layout: post
title: Button Customization| Dialog | MobileAspNetMVC | Syncfusion
description: button customization
platform: mobileaspnetmvc
control: Dialog
keywords: dialog, button
documentation: ug
---

# Button Customization

## Left button caption
 
 To specifies the text of the Left Button. The default value is Cancel.


{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Cellular Data is Turned off").LeftButtonCaption("OK").EnableAutoOpen(true).Mode(DialogMode.Confirm).Content(

@<div>

Turn on cellular data or use Wi-Fi to access data

</div>)

}
{% endhighlight %}


The following screenshot displays the output.



![](Button-Customization_images/Button-Customization_img1.png)


## Right button caption

To specifies the text of the Right Button. The default value is continue.


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


## Show buttons                                

 To show the buttons in the Dialog box. The default value is true.


{% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("London").RightButtonCaption("Continue").EnableAutoOpen(true).ShowButtons(false).Mode(DialogMode.Confirm).Content(

        @<div>

             London, one of the most popular tourist destination in the world for a reason.

        </div>)

}
{% endhighlight %}


The following screenshot displays the output.

![](Button-Customization_images/Button-Customization_img3.png)


