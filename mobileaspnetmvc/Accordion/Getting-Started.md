---
layout: post
title: Getting-Started
description: getting started
platform: mobileaspnetmvc
control: Accordion
documentation: ug
---

# Getting Started

This section briefly describes about how to create and customize Accordion widget.

Create your first Accordion in MVC

The ASP.NET MVC Mobile Accordion Control provides a way to display collapsible content panels to present information in a limited amount of space. In the following guidelines, you can learn to create a Live Soccer App and through that you can learn the features in ASP.NET MVC Accordion widget.



{ ![](Getting-Started_images/Getting-Started_img1.png) | markdownify }
{:.image }


In the above screenshot , you can click headers to expand/collapse content. You can also load content on demand, by specifing the URL to be loaded.

Create the required layout

ASP.NET MVC Accordion widget is rendered, either by specifying static content, or by using on demand contents by specifying the respective URL. Either case, Accordion control is rendered based on the default values for all the properties. You can easily customize Accordion control by changing its properties according to your requirements. In the Live Soccer App, three Panels are required; one for displaying the Recent Matches, second for listing out the Upcoming Matches and another for displaying the Ongoing MatchesUpdates on the Live Soccer App. The following steps guide you to create a basic Accordion for your application.

Create a simple MVC application and paste the following header and scrollpanel layout page content inside the <body>tag of layout.cshtml. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).



       &lt;!-- header control --&gt;

       @Html.EJMobile().Header("header").Title("Live Soccer").Render()

       &lt;div id="accordion" class="sample"&gt;

           &lt;div&gt;

                @RenderBody()

           &lt;/div&gt;

       &lt;/div&gt;

      &lt;!--Scroll Panel--&gt;

       @Html.EJMobile().Scrollpanel("acc").Target("accordion")





To render Accordion control, you can call Accordion Helper Method. You can refer the following code example and add the following Layout code to the corresponding view page.



        &lt;!--Accordion Control--&gt;

        @Html.EJMobile().Accordion("accordionControl").Items(accItem=>

             {

                 &lt;!--Accordion Item 1--&gt;

                 accItem.Add().Text("Recent Matches");



                 &lt;!--Accordion Item 2--&gt;

                 accItem.Add().Text("Upcoming Matches");



                 &lt;!--Accordion Item 3--&gt;

                 accItem.Add().Text("Ongoing Matches");



             })



Run this code to render the following output.



{ ![](Getting-Started_images/Getting-Started_img2.png) | markdownify }
{:.image }


Select the accordion item

The SelectedItems property expands the specific content section, initially by using its index value. Multiple content sections can be expanded at a time. It accepts numeric array type. The default SelectedItems value is [0]. So the first panel is in expanded state. But in this case example, you need all the panels in collapsed state, initially. So you need to set SelectedItems property with the value [-1]. 



       &lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{-1}).Items(accItem=>

            {

                  &lt;!--Accordion Item 1--&gt;

                  accItem.Add().Text("Recent Matches");



                  &lt;!--Accordion Item 2--&gt;

                  accItem.Add().Text("Upcoming Matches");



                  &lt;!--Accordion Item 3--&gt;

                  accItem.Add().Text("Ongoing Matches");

            })



{ ![](Getting-Started_images/Getting-Started_img3.png) | markdownify }
{:.image }


Enable Header icons

By default Header icons are not visible. To make the icons visible, set ShowHeaderIcon property to true.



       &lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{-1}).ShowHeaderIcon(true).Items(accItem=>

            {

                  &lt;!--Accordion Item 1--&gt;

                  accItem.Add().Text("Recent Matches");



                  &lt;!--Accordion Item 2--&gt;

                  accItem.Add().Text("Upcoming Matches");



                  &lt;!--Accordion Item 3--&gt;

                  accItem.Add().Text("Ongoing Matches");

            })



{ ![](Getting-Started_images/Getting-Started_img4.png) | markdownify }
{:.image }


Make Accordion collapsible

By default, all the content sections are not collapsible. To make all its content section as collapsible, set Collapsible property to true.



        &lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{-1}).ShowHeaderIcon(true)

.Collapsible(true).Items(accItem=>

            {

                  &lt;!--Accordion Item 1--&gt;

                  accItem.Add().Text("Recent Matches");



                  &lt;!--Accordion Item 2--&gt;

                  accItem.Add().Text("Upcoming Matches");



                  &lt;!--Accordion Item 3--&gt;

                  accItem.Add().Text("Ongoing Matches");

            })

Add content

In this use case example given, the contents of the Recent Matches and Upcoming Matches panels are given as static. In these content panels, the team results and match schedules are listed.

The following code example adds Recent Matches and Upcoming Matches panels’ content.



       &lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{1}).ShowHeaderIcon(true)

       .Collapsible(true).Items(accItem=>

           {

               &lt;!--Accordion Item 1--&gt;

               accItem.Add().Text("Recent Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

<div class="message-title">Crystal Palace – 3

                         <div class="time-panel">6th May</div>&lt;/div&gt;

                      <div class="message-title">Liverpool - 3</div>

                      <div class="text-panel">Match Drawn</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Arsenal – 1

                         <div class="time-panel">4th May</div>&lt;/div&gt;

                      <div class="message-title">West Brom - 0</div>

                      <div class="text-panel">Arsenal won the match</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                      <div class="message-title">Rayo – 0

                         <div class="time-panel">3rd May</div>&lt;/div&gt;

                      <div class="message-title">Athletic - 3</div>

                      <div class="text-panel">Athletic won the match</div>

                   &lt;/div&gt;);



               &lt;!--Accordion Item 2--&gt;

               accItem.Add().Text("Upcoming Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

<div class="message-title">Man City

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Aston Villa</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Valladolid

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Real Madrid</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Villarreal

                          <div class="time-panel">10th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Rayo</div>

                   &lt;/div&gt;);



               &lt;!--Accordion Item 3--&gt;

               accItem.Add().Text("Ongoing Matches");

            })



Use the following styles for the content style.



       &lt;style&gt;

           .appview .sample{

               padding:20px;

           }

           .appview .message-title{

              font-weight: bold;

              padding-bottom: 5px;

              padding-top: 8px;

           }

           .appview .text-panel{

              padding-bottom: 5px;

           }

           .appview .border-panel{

              border-bottom-width: 1px;

              border-bottom-color: #C0C0C0;

              border-bottom-style: solid;

              padding-top: 5px;

           }

           .appview .time-panel{

                float: right;

                font-weight: bold;

            }

      &lt;/style&gt;

{ ![](Getting-Started_images/Getting-Started_img5.png) | markdownify }
{:.image }


{ ![](Getting-Started_images/Getting-Started_img6.png) | markdownify }
{:.image }


Load content on-demand

In some cases, you can load content only when it is required. In this case, the OngoingMatches panel needs to be loaded only when you want to check for updates, since it refers a live content. To achieve this, specify AjaxUrl property with the respective URL of the view page file that contains the dynamic content.



       &lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{2}).ShowHeaderIcon(true)

       .Collapsible(true).Items(accItem=>

           {

               accItem.Add().Text("Recent Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

                   <div class="message-title">Crystal Palace – 3

                         <div class="time-panel">6th May</div>&lt;/div&gt;

                      <div class="message-title">Liverpool - 3</div>

                      <div class="text-panel">Match Drawn</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Arsenal – 1

                         <div class="time-panel">4th May</div>&lt;/div&gt;

                      <div class="message-title">West Brom - 0</div>

                      <div class="text-panel">Arsenal won the match</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                      <div class="message-title">Rayo – 0

                         <div class="time-panel">3rd May</div>&lt;/div&gt;

                      <div class="message-title">Athletic - 3</div>

                      <div class="text-panel">Athletic won the match</div>

                   &lt;/div&gt;);

               accItem.Add().Text("Upcoming Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

                   <div class="message-title">Man City

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Aston Villa</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Valladolid

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Real Madrid</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Villarreal

                          <div class="time-panel">10th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Rayo</div>

                   &lt;/div&gt;);

               accItem.Add().Text("Ongoing Matches").AjaxUrl("load");

            })



Create a new view page with the name load.cshtml and assign its URL to AjaxUrl property.

      &lt;div&gt;

        &lt;div class="message-title"&gt;

            Brighton & Hove Albion  - 1

       &lt;div class="time-panel"&gt;

            FT</div>&lt;/div&gt;

       <div class="text-panel">vs</div>

       &lt;div class="message-title"&gt;

            Derby County  - 2</div>

        &lt;div class="border-panel"&gt;&lt;/div&gt;

        &lt;div class="message-title"&gt;

            Manchester United - 3

       &lt;div class="time-panel"&gt;

            FT</div>&lt;/div&gt;

       <div class="text-panel">vs</div>

       &lt;div class="message-title"&gt;

            Hull City  -  1</div>

       &lt;div class="border-panel"&gt;&lt;/div&gt;

       &lt;div class="message-title"&gt;

            Empoli

       &lt;div class="time-panel"&gt;

            19:00</div>

        &lt;/div&gt;

       <div class="text-panel">vs</div>

       &lt;div class="message-title"&gt;

            Crotone

       &lt;/div&gt;

      &lt;/div&gt;



{ ![](Getting-Started_images/Getting-Started_img7.png) | markdownify }
{:.image }


Disable Cache

By default, Cache is enabled. So when you load the Ongoing Matches content, it loads its dynamic content, from the specified location only once. The next time, it loads the same content from Cache. In the case example, you need to load the dynamic content on every request by clicking its header. To achieve this, set EnableCache property to False.



&lt;!--Accordion Control--&gt;

       @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[]{2}).ShowHeaderIcon(true)

       .Collapsible(true).EnableCache(false).Items(accItem=>

           {

               accItem.Add().Text("Recent Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

                   <div class="message-title">Crystal Palace – 3

                         <div class="time-panel">6th May</div>&lt;/div&gt;

                      <div class="message-title">Liverpool - 3</div>

                      <div class="text-panel">Match Drawn</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Arsenal – 1

                         <div class="time-panel">4th May</div>&lt;/div&gt;

                      <div class="message-title">West Brom - 0</div>

                      <div class="text-panel">Arsenal won the match</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                      <div class="message-title">Rayo – 0

                         <div class="time-panel">3rd May</div>&lt;/div&gt;

                      <div class="message-title">Athletic - 3</div>

                      <div class="text-panel">Athletic won the match</div>

                   &lt;/div&gt;);

               accItem.Add().Text("Upcoming Matches").Content(

                  @&lt;div&gt;

                      &lt;!--Content--&gt;

                   <div class="message-title">Man City

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Aston Villa</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Valladolid

                          <div class="time-panel">8th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Real Madrid</div>

                   &lt;div class="border-panel"&gt;&lt;/div&gt;

                   <div class="message-title">Villarreal

                          <div class="time-panel">10th May</div>&lt;/div&gt;

                       <div class="text-panel">vs</div>

                       <div class="message-title">Rayo</div>

                   &lt;/div&gt;);

               accItem.Add().Text("Ongoing Matches").AjaxUrl("load");

            })



From the above steps, you have learnt how to create and customize ASP.NET MVC Mobile Accordion widget with case examples. There are more customization properties other than the one used here. To know more about the properties, you can refer the complete documentation page of Mobile Accordion widget.

