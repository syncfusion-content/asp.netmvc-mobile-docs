---
layout: post
title: Templating
description: templating
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

## Templating

Internal Template

By using template support, you can customize the appearance of the individual list item or render the whole ListView by using a single template. Setting the RenderTemplate to true and specifying the template inside the li item renders the ListView with template item.





@Html.EJMobile().ListView("templatelist").AllowScrolling(false).DataBinding(true).DataSource("window.dbitem").RenderTemplate(true)

&lt;div class="cont-bg"&gt;

    <div class="{{>Class}}">

    &lt;/div&gt;

    &lt;div class="listrightdiv"&gt;

        &lt;span class="templatetext"&gt;{{>Name}}&lt;/span&gt; &lt;span class="designationstyle"&gt;{{>Designation}}&lt;/span&gt;

        &lt;div class="aboutstyle"&gt;

{{>About}}

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;

External template

The TemplateId property is used to define the template ID for the list item. Template is defined outside and is rendered by using its ID for list items. The Template ID is set to the TemplatId property for the ListView control so that the template renders along with the ListView. To use TemplateId property, enable the RenderTemplate property.





@Html.EJMobile().ListView("ListView").HeaderTitle("Inbox").Items(items => {

       items.Add().RenderTemplate(true).TemplateId("target1");

       items.Add().RenderTemplate(true).TemplateId("target2");

       items.Add().RenderTemplate(true).TemplateId("target3");

   })

&lt;div id="target1"&gt;

        &lt;div class="content-panel"&gt;

            &lt;div class="name-panel"&gt;

                John Linden<div class="time-panel">

                    5th Jan

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;div class="message-title"&gt;

                Fw:Training

            &lt;/div&gt;

            &lt;p class="text-panel"&gt;

                All WinRT controls are optimized for touch, supporting common gestures: zooming, panning, selecting, double-tapping, rotating, resizing.

            &lt;/p&gt;

            &lt;div class="border-panel"&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div id="target2"&gt;

        &lt;div class="content-panel"&gt;

            &lt;div class="name-panel" style="padding-top: 10px;"&gt;

                David<div class="time-panel">

                    6th Jan

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;div class="message-title"&gt;

                Re:Training

            &lt;/div&gt;

            &lt;p class="text-panel"&gt;

                All the components in the ASP. NET MVC Essential Studio have been built from the ground up with performance in mind and are extremely lightweight.

            &lt;/p&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div id="target3"&gt;

        &lt;div class="content-panel"&gt;

            &lt;div class="name-panel" style="padding-top: 10px;"&gt;

                James Mario<div class="time-panel">

                    6th Jan

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;div class="message-title"&gt;

                Re:Training

            &lt;/div&gt;

            &lt;p class="text-panel"&gt;

                Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.

            &lt;/p&gt;

        &lt;/div&gt;

    &lt;/div&gt;

You can add the following styles for better appearance.

&lt;style&gt;



        .appview .e-m-android .name-panel, .appview .e-m-android .time-panel {

            color: #4DA6C4;

        }



        .appview .e-m-flat .name-panel, .appview .e-m-flat .time-panel {

            color: #F48B22;

        }



        .appview .time-panel {

            float: right;

            color: #007AFF;

            font-weight: bold;

        }



        .appview .content-panel {

            font-size: 14px;

        }



        .appview .name-panel {

            font-size: 15px;

            font-weight: bold;

            color: #007AFF;

            padding-bottom: 5px;

        }



        .appview .message-title {

            font-weight: bold;

            padding-bottom: 5px;

        }



        .appview .text-panel {

            padding-bottom: 5px;

            padding-top: 5px;

        }

    &lt;/style&gt;



The following screenshot displays the Template:

{ ![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/ListBox/images/ios7_18.png](Templating_images/Templating_img1.png) | markdownify }
{:.image }


