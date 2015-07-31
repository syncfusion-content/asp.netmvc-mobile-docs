---
layout: post
title: TemplateId
description: templateid
platform: mobileaspnetmvc
control: Header and Footer
documentation: ug
---

# TemplateId

Template ID is used to define the ID of the template element where you can specify the content to render in the control.

{% highlight html %}

@Html.EJMobile().Header("header_sample").TemplateId("template")


 <div id="template" class="temp">

@Html.EJMobile().Rating("rating") 

 </div>
 
{% endhighlight %}

The following screenshot displays the Template ID:

![F:/headertemplate.png](TemplateId_images/TemplateId_img1.png)



