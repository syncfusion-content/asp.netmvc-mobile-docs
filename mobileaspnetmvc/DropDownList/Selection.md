---
layout: post
title: Data Binding | DropDownList | MobileAspNetMVC | Syncfusion
description: data binding
platform: mobileaspnetmvc
control: DropDownList (Mobile)
documentation: ug
keywords : Selection 
---

# selection

## Multi selection

DropDownList has a check list feature that is used to select multiple list items, by using set enableMultiSelect property as true.

{% highlight html %}


          <div>
                @Html.EJMobile().DropDownList("list").WaterMarkText("Select a Country").TargetId("targetEle").EnableMultiSelect(true)
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


The following screenshot displays the the multiselection

![](Selection-images/Selection-img1.png)

