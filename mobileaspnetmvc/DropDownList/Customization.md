---
layout: post
title: Customization | DropDownList | MobileAspNetMVC | Syncfusion
description: customization
platform: mobileaspnetmvc
control: DropDownList (Mobile)
documentation: ug
keywords : watermark , height , width
---

# Customization

## Adding watermark text

It provides the short description of the expected value in dropdown and will display the text until any item is selected. You can set this text using data-ej-watermarktext attribute.

{% highlight html %}

            <div>
                @Html.EJMobile().DropDownList("list").WaterMarkText("Select a Country").TargetId("targetEle")
                <!--Adding list of options -->
                <ul id="targetEle">
                    <li data-ej-text="Australia"></li>
                    <li data-ej-text="Brazil"></li>
                    <li data-ej-text="China"></li>
                    <li data-ej-text="India"></li>
                    <li data-ej-text="Spain"></li>
                    <li data-ej-text="United States of America"></li>
                </ul>
             </div>

{% endhighlight %}


The following screenshot displays the customized watermarktext

![](Customization-images/Customization-img1.png)

## Height and width customization

You can customize the DropDownList by using data-ej-popupwidth and data-ej-popupheight attributes.

{% highlight html %}


            <div>
                @Html.EJMobile().DropDownList("list").WaterMarkText("Select a Country").TargetId("targetEle").PopupHeight("100")
                <!--Adding list of options -->
                <ul id="targetEle">
                    <li data-ej-text="Australia"></li>
                    <li data-ej-text="Brazil"></li>
                    <li data-ej-text="China"></li>
                    <li data-ej-text="India"></li>
                    <li data-ej-text="Spain"></li>
                    <li data-ej-text="United States of America"></li>
                </ul>
             </div>

{% endhighlight %}


The following screenshot displays the height and width customization of DropDownList.

![](Customization-images/Customization-img2.png)

