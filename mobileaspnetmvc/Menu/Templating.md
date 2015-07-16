---
layout: post
title: Templating
description: templating
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

## Templating

RenderTemplate

By using template support, you can customize the appearance of an individual Menu item or the whole Menu is rendered with a single template. Setting the RenderTemplate to true and specifying the template inside the li item render Menu with template item. Refer to the following code example.

&lt;div style="text-align: center;"&gt;

    @Html.EJMobile().Button("menuitem").Text("Menu")

&lt;/div&gt;

    @Html.EJMobile().Menu("menu_sample").TargetId("menuitem").RenderTemplate(true).ContentTemplate(@&lt;div style="text-align:center;"&gt;

           &lt;div&gt;&lt;img class="image" src="message.gif" /&gt;<span class="text">Message</span>&lt;/div&gt;

           &lt;div&gt;&lt;img class="image" src="mail.gif" /&gt;<span class="text">Mail</span>&lt;/div&gt;

           &lt;div&gt;&lt;img class="image" src="twitter.gif" /&gt;<span class="text">Twitter</span>&lt;/div&gt;

           &lt;div&gt;&lt;img class="image" src="facebook.gif" /&gt;<span class="text">Facebook</span>&lt;/div&gt;

        &lt;/div&gt;)

The following screenshot displays the RenderTemplate of Menu:

{ ![C:/Users/dineshr/Desktop/1.png](Templating_images/Templating_img1.png) | markdownify }
{:.image }


TemplateID

This property is used to define the Template ID for the Menu item. Template is defined outside and can be rendered by using its ID for Menu items. The template’s ID is set to the TemplatId property for the Menu control so that the template renders along with the Menu. To use TemplateId property, enable the RenderTemplate property.

&lt;div style="text-align: center;"&gt;

   @Html.EJMobile().Button("menuitem").Text("Menu")

&lt;/div&gt;

@Html.EJMobile().Menu("menu_sample").TargetId("menuitem").Items(item =>

 {

   item.Add().Text("Get info").RenderTemplate(true).TemplateId("template1");

   item.Add().Text("Show in folder").RenderTemplate(true).TemplateId("template2");

   item.Add().Text("Delete").RenderTemplate(true).TemplateId("template3");

 })



&lt;div id="template1"&gt;

     <span class="text">Insurance</span>

&lt;/div&gt;

&lt;div id="template2"&gt;

    <span class="text">Premium</span>

&lt;/div&gt;

&lt;div id="template3"&gt;

    <span class="text">Benefits</span>

&lt;/div&gt;



