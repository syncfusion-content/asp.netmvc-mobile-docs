---
layout: post 
title: Getting starting | DropDownList | MobileAspNetMVC | Syncfusion 
description: Getting starting 
platform: mobileaspnetmvc 
control: DropDownList (Mobile) 
documentation: ug
keywords: dropdownlist
---

# Getting starting

This section explains briefly about how to create a dropdownlist in your mobile  ASP.NET MVC application 
Essential JavaScript dropdownlist provides support for multiple selections, within your web page and allows you to specify an option from the list. 
The following screenshot demonstrates the functionality with dropdownlist action.

![](getting-started-images/img1.png)


## Create basic mobile layout

Create a simple MVC application and paste the following header and scrollpanel layout page content inside the <body>tag of layout.cshtml. You can create a MVC Project and add necessary Dll’s and Scripts with the help of the [MVC Getting Started Documentation](https://help.syncfusion.com/aspnetmvc/getting-started).

{% highlight html %}

  @Html.EJMobile().NavigationBar("header").Title("Dropdownlist")
  
  <div id="dropdownlist" class="sample">

            <div>

                <!--Dropdownlist  control-->

            </div>

        </div>

        <!--Scroll Panel-->
        @Html.EJMobile().Scrollpanel("acc").Target("dropdownlist")

{% endhighlight %}

## Create DropDownList control

To Create DropDownList control, specify ejmdropdownlist as data-role attribute for a &#60;input&#62; element. You can set the text for list items by using data-ej-text attribute.

{% highlight html %}


    <div>
              @Html.EJMobile().DropDownList("list").WaterMarkText("Select search engine")
    </div>
   
   <!--Adding list of Options -->
   
{% endhighlight %}

Run the above code to render the following output.

![](getting-started-images/img2.png)

## Add list of options

Specifies the Targetid attribute for  target element which consists the list of options to render DropDownList. 

{% highlight html %}

                <!--Dropdownlist  control-->
                @Html.EJMobile().DropDownList("list").WaterMarkText("Select search engine").TargetId("targetEle")
                <!--Adding list of options -->
                <ul id="targetEle">
                    <li data-ej-text="Google"></li>
                    <li data-ej-text="Bing"></li>
                    <li data-ej-text="Yahoo! Search"></li>
                    <li data-ej-text="Ask"></li>
                    <li data-ej-text="Aol Search"></li>
                    <li data-ej-text="Wow"></li>
                    <li data-ej-text="WebCrawler"></li>
                    <li data-ej-text="MyWebSearch"></li>
                    <li data-ej-text="Infospace"></li>
                    <li data-ej-text="DuckDuckGo"></li>
                    <li data-ej-text="Blekko"></li>
                    <li data-ej-text="Contenko"></li>
                </ul>

{% endhighlight %}

Run the above code to render the following output.

![](getting-started-images/img1.png)

## Css class

Sets the root class for DropDownList. This cssClass API helps to use custom skinning option for DropDownList control. By defining the root class using this API, we need to include this root class in CSS.

{% highlight html %}

                @Html.EJMobile().DropDownList("list").WaterMarkText("Select search engine").TargetId("targetEle").CssClass("customclass")
                <!--Adding list of options -->
                <ul id="targetEle">
                    <li data-ej-text="Google"></li>
                    <li data-ej-text="Bing"></li>
                    <li data-ej-text="Yahoo! Search"></li>
                    <li data-ej-text="Ask"></li>
                    <li data-ej-text="Aol Search"></li>
                    <li data-ej-text="Wow"></li>
                    <li data-ej-text="WebCrawler"></li>
                    <li data-ej-text="MyWebSearch"></li>
                    <li data-ej-text="Infospace"></li>
                    <li data-ej-text="DuckDuckGo"></li>
                    <li data-ej-text="Blekko"></li>
                    <li data-ej-text="Contenko"></li>
                </ul>

{% endhighlight %}

Run the above code to render the following output.

![](getting-started-images/img3.png)




