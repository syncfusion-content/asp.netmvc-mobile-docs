---
layout: post
title: Getting Started| Group Button | MobileAspNetMVC | Syncfusion
description: getting started
platform: mobileaspnetmvc
control: Group Button
documentation: ug
---

# Getting Started

This section briefly describes how to create a Group Button and use it in your application. 

## Create your first Group Button in MVC

The ASP.NET MVC Mobile Group Button allows you to display multiple buttons that is stacked together in a single line and appears like a navigation component. The following section explains you to create Group Button widgetusing a Mail App.

![C:/Users/ApoorvahR/Desktop/1.png](Getting-Started_images/Getting-Started_img1.png)


## Create the required Layout

The ASP.NET MVC Mobile Group Button widget is created with Radiobutton or Checkbox using the “GroupButtonType” property. In the Mail App, you can use the Radiobutton as input element to view the Mail content with three options “All”, “Read” and “Unread”. The respective content displays on clicking the specific button in the group. 

Create a MVC application and add the following code example in the <body> tag of layout.cshtml file.

You can create a MVC project and add necessary DLL’s and scripts with the help of the [MVC Getting Started Documentation.](http://help.syncfusion.com/js/)

{% highlight html %}

  <div id="page">

      @Html.EJMobile().Header("header").Title("Mail")

      <div id="grpbutton_sample" class="sample">

          <div>

                @RenderBody()

          </div>

      </div>

      <!--Scroll Panel-->

      @Html.EJMobile().Scrollpanel("grp").Target("grpbutton_sample")

  </div>

{% endhighlight %}

## Create the Group Button

To create the Group Button control, add the following code example to the corresponding view page. Also you need to specify the “GroupButtonType” and the “Name” property. 

Refer to the following code example.

{% highlight html %}

<!—Group Button Control-->

     @Html.EJMobile().GroupButton("groupbutton")

     .GroupButtonType(GroupButtonType.radio).SelectedItemIndex(0).Name("options").Buttons(button =>

       {

         button.Add().Text("All");

         button.Add().Text("Read");

         button.Add().Text("Unread");

       })

{% endhighlight %}

Add the following styles for content.

{% highlight css %}

<style>

    .appview .sample {

        padding-top: 20px;

        text-align: center;

    }



    .appview .cont-bg {

        text-align: left;

        padding-left: 20px;

        padding-right: 20px;

    }



    .appview .templatetext {

        font-size: 15px;

        font-weight: bolder;

        position: relative;

        top: 10px;

    }



    .appview .designationstyle {

        float: right;

        font-size: 12px;

        padding-top: 10px;

        position: relative;

    }



    .appview .message-title {

        font-weight: bold;

        font-size: 14px;

        padding-top: 10px;

    }



    .appview .aboutstyle {

        font-size: 14px;

        overflow: hidden;

        padding-top: 10px;

        text-align: justify;

        text-overflow: ellipsis;

        white-space: nowrap;

    }



    .appview .border-panel {

        height: 25px;

    }



    .appview .content-text {

        color: #C0C0C0;

        height: 0px;

    }

    #all,#read,#unread {

        padding-top: 20px;

    }

</style>

{% endhighlight %}

Execute the above code to render the following output.

![C:/Users/ApoorvahR/Desktop/2.png](Getting-Started_images/Getting-Started_img2.png)



## Handle Events

In the Mail App, when you navigate through different buttons the content view is changed using TouchEnd event. You can specify touchEnd property to handle the functionalities that are necessary to switch the view. 

Refer the following code example.

{% tabs %}
{% highlight html %}

@Html.EJMobile().GroupButton("groupbutton").GroupButtonType(GroupButtonType.radio).SelectedItemIndex(0).Name("options").Buttons(button =>

              {

                 button.Add().Text("All");

                 button.Add().Text("Read");

                 button.Add().Text("Unread");

              }).ClientSideEvents(evt => evt.touchEnd("onselect"))

{% endhighlight %}


{% highlight javascript %}

<script type="text/javascript">

      $(function () {//hiding read and unread elements initially

             $("#read").hide();

             $("#unread").hide();

         });

    //Touch End Event Handling

function onselect(args) {

$("#all,#read,#unread").hide();

$("#" + args.text.toLowerCase()).show();

}

   </script>

{% endhighlight %}
{% endtabs %}

In this application, you are using three options “All”, “Read” and “Unread” to view the mail contents. This is achieved using the ASP.NET MVC Mobile Listview control. 

Refer the following code to create the Listview control.

For MVC Wrapper sample, create a model file for Data Binding. Add the following model code to a CS file and save it as ListLocalData.cs.

{% highlight c# %}

    public class ListTemplate

    {

        public string Name { get; set; }

        public string Title { get; set; }

        public string Message { get; set; }

        public string Time { get; set; }

        public string Flag { get; set; }

    }



    public static class ListTemplateModel

    {

       public static List<ListTemplate> listTempSourceMail = 

                                           new List<ListTemplate>();

       public static List<ListTemplate> setListTempSourceMail()

       {

          listTempSourceMail.Add(new ListTemplate { 

          Name= "John Linden", Title = "Fw:Training", Message = "All WinRT controls  

          are optimized for touch, supporting common gestures: zooming,panning,       

          selecting, double-tapping, rotating, resizing.", Time= "20th May" 

          ,Flag = "All" });



          listTempSourceMail.Add(new ListTemplate { Name = "David", Title = 

          "Re:Training", Message = "All the components in the ASP. NET MVC Essential  

          Studio have been built from the ground up with performance in mind and are  

          extremely lightweight.", Time= "16th May" , Flag = "All" });



          listTempSourceMail.Add(new ListTemplate { Name = "Erik", Title = 

          "Re:Training", Message =  "Syncfusion Metro Studio is a collection of over  

          2500 Metro-style icon templates that can be easily customized to create  

          thousands of unique Metro icons.", Time = "10th May", Flag = "All" });



          listTempSourceMail.Add(new ListTemplate { Name = "Claire", 

          Title = "Fw:Training", Message = "All the components in the ASP. NET MVC 

          Essential Studio have been built from the ground up with performance in 

          mind and are extremely lightweight.", Time = "16th May" , Flag = "Read" });



          listTempSourceMail.Add(new ListTemplate { Name = "David", 

          Title = "Re:Training", Message = "All WinRT controls are optimized for touch, 

          supporting common gestures: zooming,panning, selecting, double-tapping,  

          rotating,resizing.", Time = "10th May" , Flag = "Read" });



          listTempSourceMail.Add(new ListTemplate { Name = "John Linden", 

          Title = "Re:Training", Message = "With our sophisiticated Direct-Trac support  

          system, built from the ground up to support enterprise customers, you will have   

          a streamlined experience working with our support team.", Time = "5th May" , 

          Flag = "Read" });



          return listTempSourceMail;

      }





      public static void clearSource()

       {

          listTempSourceMail.Clear();       

       }       

    }



Add the following code example to the corresponding controller page.


     public ActionResult sample()

       {

            ListTemplateModel.clearSource();

            ViewBag.All = ListTemplateModel.setListTempSourceMail().Where(All=>   

                                                      All.Flag.Equals("All")).ToList();

            ListTemplateModel.clearSource();

            ViewBag.Read = ListTemplateModel.setListTempSourceMail().Where(Read =>  

                                                    Read.Flag.Equals("Read")).ToList();

            return View();            

       }

{% endhighlight %}

Add the following code to the corresponding view page.

{% highlight html %}

<!--Add the Mail Content-->

       <div id="all">

            @Html.EJMobile().ListView("templatelistAll").AllowScrolling(false)

            .DataSource((List<ListTemplate>)ViewBag.All).DataBinding(true)

            .ShowHeader(false).RenderTemplate(true).ContentTemplate(

                 @<div class="cont-bg">

                      <span class="templatetext">{{>Name}}</span>

                      <span class="designationstyle">{{>Time}}</span>

                      <div class="message-title">{{>Title}}</div>

                      <div class="aboutstyle">{{>Message}}</div>

                  </div>)

       </div>

       <div id="read">

            @Html.EJMobile().ListView("templatelistRead").AllowScrolling(false)

            .DataSource((List<ListTemplate>)ViewBag.Read).DataBinding(true)

            .ShowHeader(false).RenderTemplate(true).ContentTemplate(

                 @<div class="cont-bg">

                      <span class="templatetext">{{>Name}}</span>

                      <span class="designationstyle">{{>Time}}</span>

                      <div class="message-title">{{>Title}}</div>

                      <div class="aboutstyle">{{>Message}}</div>

                   </div>)

       </div>

       <div id="unread">

            <div class="border-panel"></div>

            <div class="border-panel"></div>

            <div class="content-text">You've read all the messages in your mail</div>

            <div class="border-panel"></div>

            <div class="border-panel"></div>

       </div>

{% endhighlight %}

Execute the above code examples to render the following outputs.

![](Getting-Started_images/Getting-Started_img3.png)

![](Getting-Started_images/Getting-Started_img4.png)

![C:/Users/ApoorvahR/Desktop/5.png](Getting-Started_images/Getting-Started_img5.png)



