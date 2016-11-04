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

                @Html.EJMobile().Dialog("alertdlg").Title("London").LeftButtonCaption("Cancel").EnableAutoOpen(true).Content(@<div>

                    London, one of the most popular tourist destinations in the world for a reason.

                </div>)

            }
{% endhighlight %}


The following screenshot displays the output.

![](Auto-Open_images/Auto-Open_img1.png)



