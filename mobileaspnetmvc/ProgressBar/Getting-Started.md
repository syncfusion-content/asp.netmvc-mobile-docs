---
layout: post
title: Getting Started| ProgressBar | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: ProgressBar
keywords: progressbar, text
documentation: ug
---

# Getting Started

In this section, you can learn how to create ProgressBar and how to use it in your application.

## Create your first ProgressBar in MVC

ASP.NET MVC, Mobile ProgressBar is a simple interface that indicates the current progress of an operation, such as uploading a document. In the following guidelines, you will learn about the features in ProgressBar widget and create an App Installer.

![](Getting-Started_images/Getting-Started_img1.png)



### Create the required layout for App Installer

The ASP.NET MVC Mobile ProgressBar widget is rendered by calling ProgressBar helper method with corresponding properties. You can easily customize ProgressBar control by changing its properties according to your requirements. In the App Installer, the ProgressBar is used to show the progress of installation. 

Create a simple MVC application and paste the following header and scrollpanel layout page content inside the body tag of layout.cshtml. Paste other templates in the view page for ProgressBar creation. 

You can create an MVC Project and add necessary Dlls and script, with the help of the [MVC-Getting Started Documentation.](https://help.syncfusion.com/aspnetmvc/getting-started )


{% highlight html %}
<!-- Layout Page Content -->
<!-- header control -->
@Html.EJMobile().NavigationBar("header").Title("App Installer")

<!-- ScrollPanel -->
@Html.EJMobile().Scrollpanel("scrollpanel").Target("content")





<!-- View Page Content -->

<div id="content">

    <div>

        <!-- Add image and definition -->

        <div align="center">

            <img src="http://js.syncfusion.com/UG/Mobile/Content/debug.png" style="width: 125px;" />

        </div> <br /><br />

        <div id="definition" align="center" style="padding: 0 20px">

            <b>BUG DETECTIVE</b><br />

            Bug Detective is an open source application which integrates with web browsers to debug web development tools while you browse. We can debug HTML and JavaScript live in any web page using bug detective.

        </div><br />

        <!-- Button control -->

        <div align="center">

            @Html.EJMobile().Button("button").Text("Install").ClientSideEvents(eve => eve.TouchEnd("startProgress"))

        </div>



        <!--Add progressbar Element here-->



    </div>

</div>

{% endhighlight %}


Run the above code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img2.png)



### Create ProgressBar Control

You can call ProgressBar helper to render ProgressBar control. You can set its initial value by using Value property. By default, it takes parent’s width. But, you can customize it by using Width property.

{% highlight html %}

 <!--ProgressBar control -->


      @Html.EJMobile().ProgressBar("progress").Value(73)


{% endhighlight %}

You can hide ProgressBar, with desired action on its hide API and you can show it with desired action on its show API.

{% highlight javascript %}

<script>

$(function () {

window.progressObject = $("#progress").data("ejmProgress"); // create object for progressbar

$("#progress").hide();//to hide progressbar at initialize

});

function startProgress(args) {

$(".e-m-btnwrapper").hide();//to hide button

$("#progress").show();// to show progressbar

}

</script>

{% endhighlight %}

Run the above code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img3.png)



### Customize Text

The default text of ProgressBar is downloading. In this scenario you are installing the app, not downloading it. So, to change the text of ProgressBar, you can use the Text property. Add the following code example to the ProgressBar helper.

{% highlight html %}

<!-- Progressbar control -->

<div style="width: 75%; margin:auto;">

  @Html.EJMobile().ProgressBar("progress").Value(73).EnableCustomText(true).Text("Installing..")

 </div>

{% endhighlight %}

Run the above code example and you can see the following output.

![](Getting-Started_images/Getting-Started_img4.png)



### Customize Text and Value Dynamically

The ProgressBar text and its value can be changed dynamically. In this scenario, to indicate the progress of installation, its value dynamically changes when you click the Install button. And when it reaches 100%, then the ProgressBar text will change from Installingto Completed. Here, its value must start from zero, so that the Value property is removed and modifies the following code example.  

{% highlight html %}

<!-- Progressbar control -->



@Html.EJMobile().ProgressBar("progress").EnableCustomText(true).Text("Installing..")

@* Value(73) is removed here *@


{% endhighlight %}

You can use setInterval function in JavaScript to change its value and text dynamically.

{% highlight javascript %}

<script>

window.currValue = 0;

$(function () {

window.progressObject = $("#progress").data("ejmProgress"); // create object for progressbar

$("#progress").hide(); //to hide progressbar at starting

});

function startProgress(args) {

$(".e-m-btnwrapper").hide(); //to hide button

$("#progress").show(); // to show progressbar

window.timeInterval = setInterval(runProgress, 100); //set time intervel to repeat the process

}

function runProgress() {

progressObject.option("value", window.currValue); //set value for progress

var value = currValue++;

if (value == 100) {

progressObject.option("text", "Completed..."); // change the text when it reaches 100%

clearInterval(window.timeInterval); //to clear time interval

}

}

    </script>


{% endhighlight %}


Run the above code example and you can see the following output, after you click the Install button. The following output is taken after the ProgressBar value reaches 100%. The text of the ProgressBar is changed in the following output.	



![](Getting-Started_images/Getting-Started_img5.png)



