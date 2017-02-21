---
layout: post
title: Getting Started| Accordion | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Accordion
documentation: ug
keywords: accordion, expand, collapse

---

# Getting Started

This section briefly describes about how to create and customize Accordion widget.

## Create your first Accordion in MVC

The ASP.NET MVC Mobile Accordion Control provides a way to display collapsible content panels to present information in a limited amount of space. In the following guidelines, you can learn to create a Live Soccer App and through that you can learn the features in ASP.NET MVC Accordion widget.

![](Getting-Started_images/Getting-Started_img1.png)



In the above screenshot , you can click headers to expand/collapse content. You can also load content on demand, by specifing the URL to be loaded.

## Create the required layout

ASP.NET MVC Accordion widget is rendered, either by specifying static content, or by using on demand contents by specifying the respective URL. Either case, Accordion control is rendered based on the default values for all the properties. You can easily customize Accordion control by changing its properties according to your requirements. In the Live Soccer App, three Panels are required; one for displaying the Recent Matches, second for listing out the Upcoming Matches and another for displaying the Ongoing MatchesUpdates on the Live Soccer App. The following steps guide you to create a basic Accordion for your application.

Create a simple MVC application and paste the following header and scrollpanel layout page content inside the <body>tag of layout.cshtml. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started).


{% highlight html %}
       <!-- header control -->

       @Html.EJMobile().NavigationBar("header").Title("Live Soccer")

       <div id="accordion" class="sample">

           <div>

                    <!--Accordion control-->

           </div>

       </div>

      <!--Scroll Panel-->

       @Html.EJMobile().Scrollpanel("acc").Target("accordion")
       
{% endhighlight %}




To render Accordion control, you can call Accordion Helper Method. You can refer the following code example and add the following Layout code to the corresponding view page.


{% highlight html %}
        <!--Accordion Control-->

   @Html.EJMobile().Accordion("accordionControl").Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches");

                 accItem.Add().Text("Upcoming Matches");

                 accItem.Add().Text("Ongoing Matches");

             })

{% endhighlight %}

Run this code to render the following output.



![](Getting-Started_images/Getting-Started_img2.png)



## Select the accordion item

The SelectedItems property expands the specific content section, initially by using its index value. Multiple content sections can be expanded at a time. It accepts numeric array type. The default SelectedItems value is [0]. So the first panel is in expanded state. 


{% highlight html %}
       <!--Accordion Control-->

      @Html.EJMobile().Accordion("accordionControl").SelectedItems(new int[] { 1 }).Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches");

                 accItem.Add().Text("Upcoming Matches");

                 accItem.Add().Text("Ongoing Matches");

             })


{% endhighlight %}


![](Getting-Started_images/Getting-Started_img3.png)



## Enable expand and collapse icons

By default Header icons are  visible. To make the icons invisible, set "ShowHeaderIcon" property to false.


{% highlight html %}
       <!--Accordion Control-->

          @Html.EJMobile().Accordion("accordionControl").ShowHeaderIcon(true).Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches");

                 accItem.Add().Text("Upcoming Matches");

                 accItem.Add().Text("Ongoing Matches");

             })

{% endhighlight %}


![](Getting-Started_images/Getting-Started_img4.png)



## Make Accordion collapsible

By default, all the content sections are not collapsible. To make all its content section as collapsible, set 'CollapseAll' property to true.


{% highlight html %}
        <!--Accordion Control-->
    @Html.EJMobile().Accordion("accordionControl").CollapseAll(true).Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches");

                 accItem.Add().Text("Upcoming Matches");

                 accItem.Add().Text("Ongoing Matches");

             })
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img8.png)

## Add content

In this use case example given, the contents of the Recent Matches and Upcoming Matches panels are given as static. In these content panels, the team results and match schedules are listed.

The following code example adds Recent Matches and Upcoming Matches panels’ content.


{% highlight html %}
       <!--Accordion Control-->

     @Html.EJMobile().Accordion("accordionControl").Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches").Content(
                    @<div>
                        <div class="message-title">
                            Crystal Palace – 3
                            <div class="time-panel">6th May</div>
                        </div>
                        <div class="message-title">Liverpool - 3</div>
                        <div class="text-panel">
                            Match Drawn
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Arsenal – 1
                            <div class="time-panel">4th May</div>
                        </div>
                        <div class="message-title">West Brom - 0</div>
                        <div class="text-panel">
                            Arsenal won the match
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Rayo – 0
                            <div class="time-panel">3rd May</div>
                        </div>
                        <div class="message-title">Athletic - 3</div>
                        <div class="text-panel">
                            Athletic won the match
                        </div>

                    </div>); 

                 accItem.Add().Text("Upcoming Matches").Content(@<div>
            <div class="message-title">
                Man City
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Aston Villa
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Valladolid
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Real Madrid
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Villarreal
                <div class="time-panel">10th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Rayo
            </div>
        </div>);

                 accItem.Add().Text("Ongoing Matches");
             })
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img5.png)


## Load content on-demand

In some cases, you can load the Ajax content. content only when it is required. In this case, the OngoingMatches panel needs to be loaded only when you want to check for updates, since it refers a live content. To achieve this, specify AjaxUrl property with the respective URL of the view page file that contains the dynamic content.Specify “Href” attribute with the respective URL of the HTML file that contains the dynamic content. The data-ej-spinnertext attribute is used to show the loading text, while getting (waiting for) the response from the server (via Ajax request).

{% highlight html%}

       <!--Accordion Control-->


    @Html.EJMobile().Accordion("accordionControl").EnableAjax(true).Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches").Content(
                    @<div>
                        <div class="message-title">
                            Crystal Palace – 3
                            <div class="time-panel">6th May</div>
                        </div>
                        <div class="message-title">Liverpool - 3</div>
                        <div class="text-panel">
                            Match Drawn
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Arsenal – 1
                            <div class="time-panel">4th May</div>
                        </div>
                        <div class="message-title">West Brom - 0</div>
                        <div class="text-panel">
                            Arsenal won the match
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Rayo – 0
                            <div class="time-panel">3rd May</div>
                        </div>
                        <div class="message-title">Athletic - 3</div>
                        <div class="text-panel">
                            Athletic won the match
                        </div>

                    </div>);

                 accItem.Add().Text("Upcoming Matches").Content(@<div>
            <div class="message-title">
                Man City
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Aston Villa
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Valladolid
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Real Madrid
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Villarreal
                <div class="time-panel">10th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Rayo
            </div>
        </div>);
                 accItem.Add().Text("Ongoing Matche").Href(@Url.Content("~/accordion/load")); 
             });

{% endhighlight %}


Create a new view page with the name load.cshtml and assign its URL to AjaxUrl property.


{% highlight html%}
      <div>

      <div class="message-title">
                Brighton & Hove Albion  - 1
                <div class="time-panel">FT</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Derby County  - 2
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Manchester United - 3

                <div class="time-panel">Ft</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Hull City  -  1
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Empoli
                <div class="time-panel">
                    19/div>
                </div>
                <div class="text-panel">vs</div>
                <div class="message-title">
                    Crotone
                </div>
            </div>
{% endhighlight %}



![](Getting-Started_images/Getting-Started_img7.png)



## Disable Cache

By default, Cache is disabled. So when you load the Ongoing Matches content, it loads its dynamic content, from the specified location only once. The next time, it loads the same content from Cache. In the case example, you need to load the dynamic content on every request by clicking its header. To achieve this, set EnableCache property to False.


{% highlight html%}
<!--Accordion Control-->

      
    @Html.EJMobile().Accordion("accordionControl").EnableCache(true).EnableAjax(true).Items(accItem =>
             {

                 accItem.Add().Text("Recent Matches").Content(
                    @<div>
                        <div class="message-title">
                            Crystal Palace – 3
                            <div class="time-panel">6th May</div>
                        </div>
                        <div class="message-title">Liverpool - 3</div>
                        <div class="text-panel">
                            Match Drawn
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Arsenal – 1
                            <div class="time-panel">4th May</div>
                        </div>
                        <div class="message-title">West Brom - 0</div>
                        <div class="text-panel">
                            Arsenal won the match
                        </div>
                        <div class="border-panel"></div>
                        <div class="message-title">
                            Rayo – 0
                            <div class="time-panel">3rd May</div>
                        </div>
                        <div class="message-title">Athletic - 3</div>
                        <div class="text-panel">
                            Athletic won the match
                        </div>

                    </div>);

                 accItem.Add().Text("Upcoming Matches").Content(@<div>
            <div class="message-title">
                Man City
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Aston Villa
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Valladolid
                <div class="time-panel">8th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Real Madrid
            </div>
            <div class="border-panel"></div>
            <div class="message-title">
                Villarreal
                <div class="time-panel">10th May</div>
            </div>
            <div class="text-panel">vs</div>
            <div class="message-title">
                Rayo
            </div>
        </div>);
                 accItem.Add().Text("Ongoing Matche").Href(@Url.Content("~/accordion/load")); 
             });

{% endhighlight %}


From the above steps, you have learnt how to create and customize ASP.NET MVC Mobile Accordion widget with case examples. There are more customization properties other than the one used here. To know more about the properties, you can refer the complete documentation page of Mobile Accordion widget.

