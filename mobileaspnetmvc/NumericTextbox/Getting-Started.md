---
layout: post
title: Getting Started| Numeric Textbox | MobileAspNetMVC | Syncfusion
description: getting started 
platform: mobileaspnetmvc
control: Numeric Textbox
documentation: ug
---

# Getting started 

In this section you can learn how to create first Numeric Textbox Control in mobile application.

## Create your first Numeric Textbox in MVC

The following is an example for Rooms Availability Check and it describes how simple it is to create the first layout of Numeric Textbox and how efficient it is to use the features of the control.

### Create the required layout

You can render the Numeric Textbox control based on the default values for all the properties. You can easily customize Numeric Textbox control by changing their properties according to your requirements.

You can create an MVC Project and add necessary assemblies, styles and scripts to it.  Refer [MVC-Getting Started.](http://help.syncfusion.com/aspnetmvc/captcha/getting-started#create-your-first-captcha-in-aspnet-mvc )

1. Create a View page and add the following template.
   
{% highlight html %}
		<!--Page Header-->
		@Html.EJMobile().NavigationBar("page_header").Title("Rooms Availability").Mode(NavBarMode.Header).Position(NavBarPosition.Auto)
		<div id="content" class="content">
		<div class="content_area">
		<!--Numeric TextBox 1 code here-->
		<!--Numeric TextBox 2 code here-->
		<div class="text_row button_cnt">
		@Html.EJMobile().Button("but_submit").Text("Check Availability")                        
		</div>
		</div>
		</div>    
{% endhighlight %}
   

2. Add the following code example to render Numeric Textbox to input number of persons per room.

{% highlight html %}
   
			<!--Numeric TextBox 1 code-->
			<div class="text_row">
			<label>No of person per room :</label>
			@Html.EJMobile().NumericTextbox("persontext").MinimumValue(1).MaximumValue(6)
			</div>
			
{% endhighlight %}	



3. Add the following code example to render Numeric Textbox to input number of rooms needed.

{% highlight html %}
   
		<!--Numeric TextBox 2 code-->
		<div class="text_row">
		<label>No of rooms :</label>
		@Html.EJMobile().NumericTextbox("roomstxt").MinimumValue(1).MaximumValue(5)
		</div>
   
{% endhighlight %}
   


4. To improve the look and feel of Rooms Availability Check, you need to add the following styles in the application.
   
{% highlight css %}
   
		<style>
		.content_area {
		margin-top: 45px;
		padding: 20px;
		}
		.content {
		max-width: 480px;
		margin: 0 auto;
		}
		.text_row {
		margin-top: 25px;
		}
		.button_cnt {
		width: 160px;
		margin-left: auto;
		margin-right: auto;
		}
		</style>

{% endhighlight %}
   
![](Getting-Started_images/Getting-Started_img1.png)