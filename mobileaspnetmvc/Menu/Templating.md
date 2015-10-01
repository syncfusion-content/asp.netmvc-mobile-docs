---
layout: post
title: Templating| Menu | MobileAspNetMVC | Syncfusion
description: templating
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Templating

## RenderTemplate

By using template support, you can customize the appearance of an individual Menu item or the whole Menu is rendered with a single template. Setting the RenderTemplate to true and specifying the template inside the li item render Menu with template item. Refer to the following code example.

{% highlight html %}

<div style="text-align: center;">

@Html.EJMobile().Button("menuitem").Text("Menu")

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").RenderTemplate(true).ContentTemplate(@<div style="text-align:center;">

<div><img class="image" src="message.gif" /><span class="text">Message</span></div>

<div><img class="image" src="mail.gif" /><span class="text">Mail</span></div>

<div><img class="image" src="twitter.gif" /><span class="text">Twitter</span></div>

<div><img class="image" src="facebook.gif" /><span class="text">Facebook</span></div>

</div>)
		
{% endhighlight %}

The following screenshot displays the RenderTemplate of Menu:

![C:/Users/dineshr/Desktop/1.png](Templating_images/Templating_img1.png)



## TemplateID

This property is used to define the Template ID for the Menu item. Template is defined outside and can be rendered by using its ID for Menu items. The template’s ID is set to the TemplatId property for the Menu control so that the template renders along with the Menu. To use TemplateId property, enable the RenderTemplate property.

{% highlight html %}

<div style="text-align: center;">

   @Html.EJMobile().Button("menuitem").Text("Menu")

</div>

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").Items(item =>

 {

   item.Add().Text("Get info").RenderTemplate(true).TemplateId("template1");

   item.Add().Text("Show in folder").RenderTemplate(true).TemplateId("template2");

   item.Add().Text("Delete").RenderTemplate(true).TemplateId("template3");

 })



<div id="template1">

     <span class="text">Insurance</span>

</div>

<div id="template2">

    <span class="text">Premium</span>

</div>

<div id="template3">

    <span class="text">Benefits</span>

</div>

{% endhighlight %}

