---
layout: post
title: Getting Started| SplitPane | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: SplitPane
documentation: ug
---

# Getting Started

This section enables you to create SplitPane using JavaScript in your mobile app.

## Create your first SplitPane in MVC

The Essential Studio for ASP.NET MVC Mobile Splitpane divides a region on the web page.  It is configured to split up the horizontal view vertically. Right side panes can display the content from an external URL that is specific to the item selected in the left pane. In the following guidelines, you can learn the features in Splitpane widget by creating a Mail App.

![](Getting-Started_images/Getting-Started_img1.png)



### Create the Splitpane control

The Essential Studio for ASP.NET MVC MobileSplitpane control is rendered by calling the Splitpane Helper. 

Create a simple MVC application and add the following code example in the view page named as SplitPaneSample for Splitpane creation. For creating a MVC Project, adding necessary Dll’s and Scripts can be done with help of the MVC-Getting Started Documentation.

{% highlight html %}


@Html.EJMobile().SplitPane("splitview").LeftPaneTemplate(@<div></div>)


{% endhighlight %}



Run this code example and the following output is displayed. For more details, to run the samples refer "Common Getting Started" section.



![](Getting-Started_images/Getting-Started_img2.png)



### Add left Pane content

In the Left Pane, you can add listbox for easy navigation. To provide data source for listbox template in the Left Pane content, you can create a ListTemplate.cs file in the model and add the following code example to the file.


{% highlight c# %}

    public class ListTemplate

    {

        public string Name { get; set; }

        public string Time { get; set; }

        public string About { get; set; }

        public string Url { get; set; }

    }

    public static class ListTemplateModal

    {

        public static List<ListTemplate> listTempSource = new List<ListTemplate>();

        public static List<ListTemplate> setListTempSource()

        {

            listTempSource.Add(new ListTemplate { Name = "Skype", Time = "3:06 am", About = "Password changed successfully", Url = "load1" });

            listTempSource.Add(new ListTemplate { Name = "Skype", Time = "3:00 am", About = "Your password has been changed", Url = "load2" });

            listTempSource.Add(new ListTemplate { Name = "Skype", Time = "Yesterday", About = "Password token", Url = "load3" });

            listTempSource.Add(new ListTemplate { Name = "Skype", Time = "Monday", About = "Hello from Skype", Url = "load4" });

            return listTempSource;

        }

        public static void clearSource()

        {

            listTempSource.Clear();

        }       

    }

{% endhighlight %}

In the controller for the view page, add the following code example.

{% highlight c# %}

        public ActionResult SplitPaneSample()

        {

            ListTemplateModal.clearSource();

            return View(ListTemplateModal.setListTempSource());

        }


{% endhighlight %}

Create a partial view page with the name “ListViewContent.cshtml” and add the following code example to the file.

{% highlight html %}

@model List<ListTemplate>


@{

@Html.EJMobile().ListView("templatelist").AllowScrolling(true).ShowHeader(false).RenderTemplate(true).DataSource(Model).PersistSelection(true).SelectedItemIndex(0).ClientSideEvents(evt => { evt.TouchEnd("listItemSelect"); }).ContentTemplate(



    @<div class="cont-bg">



        <span class="templatetext">{{>Name}}</span> <span class="timestyle">{{>Time}}</span>



        <div class="aboutstyle">



{{>About}}

        </div>



    </div>)

}

{% endhighlight %}

Title of the Left Pane is set using LeftHeaderSettings property. In this case, you can set the title as “Inbox”. In the same way, you can set the title for Right Pane by using RightHeaderSettings property. In android mode you don’t have header, instead toolbar is present. To set title for toolbar, use the ToolbarSettings property.

Refer the following code example. The partial view (ListViewContent) is called to render the Left Pane content.

{% highlight html %}

@Html.EJMobile().SplitPane("splitview").LeftHeaderSettings(left => left.Title("Inbox")).RightHeaderSettings(right => right.Title("Message")).ToolbarSettings(tool => tool.Android(and => and.Title("Inbox"))).LeftPaneTemplate(@<div>@Html.Partial("ListViewContent")</div>)

{% endhighlight %}

Use the following styles to apply style for ListView template.

{% highlight css %}

<style type="text/css">

    .cont-bg {

        padding: 6px 0px;

    }



    .templatetext {

        font-weight: bolder;

        font-size: 17px;

    }



    #templatelist .timestyle {

        float: right;

        font-size: 12px;

        position: relative;

        right: 25px;

        padding-right: 5px;

    }



    #templatelist .aboutstyle {

        font-size: 14px;

    }



    .e-m-ios7.e-m-tablet .e-m-state-active .e-m-list-div * {

        color: #FFFFFF;

    }



    #splitview.e-m-windows.e-m-dark .e-m-sp-left {

        background: black;

    }

</style>


{% endhighlight %}

Run this code example and the following output is displayed. For more details, to run the samples refer "Common Getting Started" section.

![](Getting-Started_images/Getting-Started_img3.png)



### Add right Pane content

Refer to the following code example.

{% highlight javascript %}

<script type="text/javascript">



    // initial loading right pane content



    $(document).ready(function () {



        // $("#splitview").data("ejmSplitPane").loadContent(toPage, options)



        var split = $("#splitview").data("ejmSplitPane");

        var args = $('#templatelist').ejmListView('instance');

        split.loadContent(args.model.dataSource[0].Url, {



            rightHeaderSettings:

            { title: args.model.dataSource[0].About },

            toolbarSettings: { android: { title: args.model.dataSource[0].About } },

            transition: "none"



        });



    });







    // loading right pane content by clicking list item selected



    function listItemSelect(args) {



        // $("#splitview").data("ejmSplitPane").loadContent(toPage, options)



        var split = $("#splitview").data("ejmSplitPane");



        split.loadContent(args.model.dataSource[args.index].Url, {



            rightHeaderSettings:

            { title: args.model.dataSource[args.index].About },

            toolbarSettings: { android: { title: args.model.dataSource[args.index].About } },

            transition: "none"



        });



    }



</script>

{% endhighlight %}

Create a view page with name load1.cshtml and add the following code example to the file.

{% highlight html %}

<h2>

    Hi John,</h2>

<br />

<h3>

    Password successfully changed</h3>

<br />

Your new Skype password has been set.

<br />

You can now access your Account, view your call history or change your account settings.

<br />

<br />

<h5>

    Talk soon,</h5>

The people at Skype



Create a view page with name load2.cshtml and add the following code example to the file.

<h2>

    Hello John,</h2>

<br />

<h3>

    Your password has been changed</h3>

<br />

Your Skype password has been changed. If you did not change this yourself please

contact one of the administrators of the Skype Manager you belong to.

<br />

<br />

<h5>

    Talk soon,</h5>

The people at Skype



Create a view page with name load3.cshtml and add the following code example to the file,

<h2>

    Hello John,</h2>

<br />

<h3>

    Password token</h3>

<br />

Reset your password with this temporary code. Please note that this link is only

active for 6 hours after receipt. After the time limit expires, the code does not

work and you have to resubmit the password change request.<br />

<br />

If the link doesn't work, you can enter the code manually using this token: 45c5chg15ae33c438ch2cc7ehn004hg6

<br />

<br />

<h5>

    Talk soon,</h5>

The people at Skype



Create a view page with name load4.cshtml and add the following code example to the file,

<h3>

    Hi John,</h3>

<br />

<h2>

    Welcome to Skype</h2>

<br />

Congratulations on joining Skype! Now you can enjoy the magic of free face-to-face

calls, instant messaging, screen sharing and so much more - all with Skype.

<br />

<br />

<h5>

    Talk soon,</h5>

The people at Skype

{% endhighlight %}

Run this code example and the following output is displayed. For more details, to run the samples refer "Common Getting Started" section.

![](Getting-Started_images/Getting-Started_img4.png)



