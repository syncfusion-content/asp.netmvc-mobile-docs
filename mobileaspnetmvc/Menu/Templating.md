---
layout: post
title: Templating| Menu | MobileAspNetMVC | Syncfusion
description: templating
platform: mobileaspnetmvc
control: Menu
documentation: ug
keywords: template
---

# Templating

## Templating

You can customize the appearance of an individual Menu item or the whole Menu is rendered with a single template.

{% highlight html %}
                  <div style="text-align: center;">

                        @Html.EJMobile().Button("menuitem").Text("Menu")

                    </div>

                    @Html.EJMobile().Menu("menu_sample").Target("menuitem").ContentTemplate(@<div style="text-align:center;">

                        <div><img class="image" src="twitter.gif" /><span class="text">Twitter</span></div>

                        <div><img class="image" src="facebook.gif" /><span class="text">Facebook</span></div>

                    </div>)

		
{% endhighlight %}

The following screenshot displays the RenderTemplate of Menu:

![](Templating_images/Templating_img1.png)



## TemplateID

This property is used to define the Template ID for the Menu item. Template is defined outside and can be rendered by using its ID for Menu items. The template’s ID is set to the TemplatId property for the Menu control so that the template renders along with the Menu. 
{% highlight html %}

<div style="text-align: center;">

   @Html.EJMobile().Button("menuitem").Text("Menu")

</div>

  @Html.EJMobile().Menu("menu_sample").Target("menuitem").TemplateId("menuTemplate").ContentTemplate(@<div id="menuTemplate">
    <ul>
        <li>Get info</li>
        <li>Show in folder</li>
        <li>Delete</li>
    </ul>
</div>)

{% endhighlight %}

