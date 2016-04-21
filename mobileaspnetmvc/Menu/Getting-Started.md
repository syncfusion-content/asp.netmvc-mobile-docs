---
layout: post
title: Getting Started| Menu | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Getting Started

This section explains you on how to create a Menu using Essential ASP.NET MVC and how to use it in your application.

## Create your first Menu in MVC

The ASP.NET MVC Mobile Menu provides you an interface to easily navigate hierarchical data.  In the following section, you can learn to create a Gallery app and learn the features in Menu widget. 

![1](Getting-Started_images/Getting-Started_img1.png)


##Create the required layout for Gallery app

The ASP.NET MVCMobile Menu widget can be rend from a hierarchy of items and perform unique actions based on the properties set to each item. You can easily customize Menu control by changing its properties. The following code example illustrates the Gallery app Menu that is used to show multiple sharing options to share images. 

Create a simple MVC application and add the following code example in the <body> tag of Layout.cshtml file.

{% highlight html %}

<div id="page" data-role="appview">

        <!-- header helper -->

@Html.EJMobile().Header("menuitems").Position(MobileHeaderPosition.Normal).Title("Gallery").ShowRightButton(true).RightButtonCaption("Share")      

 <div id="content">

 <div>

 <div>

  @RenderBody()

 </div>

 </div>

 </div>

 <!-- ScrollPanel helper -->

@Html.EJMobile().Scrollpanel("scroll").Target("content")

</div>

{% endhighlight %}



Use the following styles for content.

{% highlight css %}

<style>

.appview.e-m-windows.e-m-light {



background: none repeat scroll 0 0 #eee;



}

</style> 

{% endhighlight %}

To create a Menu, add the following code example to the corresponding view page.

{% highlight html %}

<!-- Add Gallery image -->

<div align="center">

<img src="http://js.syncfusion.com/UG/Mobile/Content/wheat.jpg" style="width: 270px;

padding-top: 10%; height: 170px;" /></div>

<!-- dialog helper -->

@Html.EJMobile().Dialog("alertdlg").Title("Dialog").EnableAutoOpen(false).LeftButtonCaption("OK").ClientSideEvents(events => { events.ButtonTap("alertClose"); }).Content(@<div

    id="dialogContent">

</div>)

<!—Add Menu helper here-->

{% endhighlight %}

Execute the above code to render the following output.

![2](Getting-Started_images/Getting-Started_img2.png)


Gallery App with Share button
{:.caption}

## Create the Menu control

To render Menu control use EJmobile Menu helper. Type property allows you to set the Menu display behavior. ShowTitle property is used to enable or disable the Menu title. Menu items are added by using the Items collection and you can name each item using the Text property. 

Refer to the following code example.

{% highlight html %}

 <!-- Menu helper -->

        @Html.EJMobile().Menu("menuitem").IOS7(ios7 => ios7.ShowTitle(false)).Items(items =>

{



items.Add().Text("Twitter");



items.Add().Text("Whatsapp");



items.Add().Text("Facebook");



}) 

{% endhighlight %}

## Show the Menu

You can click the share button present in the header to display the Menu. You can achieve this by setting the targetid property as share button’s id. 

Refer to the following code example.

{% highlight html %}

        @Html.EJMobile().Menu("menuitem").TargetId("menuitems_rightbutton").IOS7(ios7 => ios7.ShowTitle(false)).Items(items =>

{



items.Add().Text("Twitter");



items.Add().Text("Whatsapp");



items.Add().Text("Facebook");



})  

{% endhighlight %}

Execute the above code and the following output displays when you click the share button.



![1](Getting-Started_images/Getting-Started_img3.png)



## Handle Menu events

TouchEnd event is handled to add functionalities to each Menu item. This is achieved using the ClientSideEvents property. When you click a particular Menu item, its corresponding TouchEnd event action is triggered and handled as illustrated in the following code example.

Add the following code example to the Menu control and the script code to the view page.


{% tabs %}
{% highlight html %}
<!-- Menu helper -->        
@Html.EJMobile().Menu("menuitem").TargetId("menuitems_rightbutton").IOS7(ios7 => ios7.ShowTitle(false)).ClientSideEvents
(events => { 
events.TouchEnd("showDialog"); 
}).Items(items =>      
 {           items.Add().Text("Twitter");           items.Add().Text("Whatsapp");           items.Add().Text("Facebook");      
 })
 
 {% endhighlight %} 

{% highlight javascript %} 
<script>      
//object declaration        
$(document).ready(function () 
{            window.menuObject = $("#menuitem").data("ejmMenu");
 // create object for menu.           
 window.dialogObject = $("#alertdlg").data("ejmDialog"); 
 // create object for dialog.          
 if (ej.isWindows() && ej.isMobile())               
 $("#menuitem").ejmMenu("model.theme", "light");        });
 //handling menu action <br>        
 //to show Dialog       
  function showDialog(args) 
 {            var text = args.text;
  //to get menu item text           
 $("#dialogContent").append("Content shared in " + text + " successfully"); 
 // add content to dialog           
 window.menuObject.hide(); 
 // to hide menu            
 window.dialogObject.open(); 
 //to open dialog        
 }        
 //to close dialog       
  function alertClose(args)
 {           
 $("#dialogContent").empty(); 
 //to empty the dialog content          
   window.dialogObject.close(); 
 //to close dialog       
 } 
 </script> 
 {% endhighlight %}    
{% endtabs %}


Execute the above code and the following output displays when you click the particular Menu item present in the Menu control.



![3](Getting-Started_images/Getting-Started_img4.png)



