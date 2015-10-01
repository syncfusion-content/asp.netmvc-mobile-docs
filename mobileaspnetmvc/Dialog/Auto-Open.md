---
layout: post
title: Auto Open| Dialog | MobileAspNetMVC | Syncfusion
description: auto open
platform: mobileaspnetmvc
control: Dialog
documentation: ug
---

# Auto Open

The EnableAutoOpen property is used to open the Dialog box on initial loading. The default value is false.


{% highlight html %}
@{

@Html.EJMobile().Dialog("alertdlg").Title("Welcome to Syncfusion").LeftButtonCaption("Cancel").EnableAutoOpen(true).Content(@<div>

Syncfusion provides software components and tools for the Microsoft .NET platform

</div>)

}
{% endhighlight %}


The following screenshot displays the output.

![](Auto-Open_images/Auto-Open_img1.png)



