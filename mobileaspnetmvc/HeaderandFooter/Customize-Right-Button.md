---
layout: post
title: Customize-Right-Button
description: customize right button
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# Customize Right Button

ShowRightButton

In Footer control, you can view the next page by using the ShowRightButton. You can manually enable/disable the button by setting true/false using ShowRightButton property.

@Html.EJMobile().Footer("footer_sample").ShowRightButton(true)

The following screenshot displays the output.

{{ '![](Customize-Right-Button_images/Customize-Right-Button_img1.png)' | markdownify }}
{:.image }


RightButtonCaption 

To specify the caption (text) for Footer Right Button, set RightButtonCaption property. 

@Html.EJMobile().Footer("footer_sample").ShowRightButton(true).RightButtonCaption("Next")     

The following screenshot displays the output.

{{ '![](Customize-Right-Button_images/Customize-Right-Button_img2.png)' | markdownify }}
{:.image }


RightButtonNavigationURL

Specifies the URL to which the page should be navigated when the Right Button is clicked.

@Html.EJMobile().Footer("footer_sample").ShowRightButton(true).RightButtonNavigationUrl("")

TemplateId

Footer has template support feature. The templateID property is used to define the ID of the template element where you can specify the content to render in the Footer. 

@Html.EJMobile().Footer("footer_sample").TemplateId("template")



 <div id="template" class="temp">

@Html.EJMobile().Rating("rating") 

 </div> 

The following screenshot displays the output.

{{ '![F:/ios7_phone.png](Customize-Right-Button_images/Customize-Right-Button_img3.png)' | markdownify }}
{:.image }


