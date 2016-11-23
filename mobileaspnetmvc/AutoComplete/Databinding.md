---
layout: post
title: Databinding| AutoComplete  | MobileAspNetMVC | Syncfusion
description: databinding
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
---

# Databinding

## Local Databinding

DataSource property is used to provide the suggestion list to the AutoComplete textbox. The list of items are passed as an array and by using the DataSource property, AutoComplete retrieves the suggestion list. Field property is used to map the specific field name of the given DataSource to render the suggestion list when user type is in the textbox. You can refer to the following code example.


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name"))
{% endhighlight %}


For MVC, you need to pass the data through model. The code example defines the model with user-defined class.


{% highlight c# %}
  public class Cars

    {

        public string name { get; set; }

    }

    public static class carsModel  

    {

        public static List<Cars> source = new List<Cars>();

        public static List<Cars> setSource()

        {

            source.Add(new Cars { name = "Audi S6" });

            source.Add(new Cars { name = "BMW 7" });

            source.Add(new Cars { name = "Chevrolet Camaro" });

            source.Add(new Cars { name = "Duesenberg J" });

            source.Add(new Cars { name = "Elantra" });

            return source;

        }

    }
{% endhighlight %}


After creating the model, pass the data to the View through Controller.


{% highlight c# %}
public class AutoCompleteController : ApplicationController

    {       

        public ActionResult DefaultFunctionalities()

        {

            return View(carsModel.setSource());

        }

     }
{% endhighlight %}



The following screenshot displays the DataSource:

![](Databinding_images/Databinding_img1.png)



## Remote Databinding

Mapper property is used to specify the remote URL of the DataSource for the suggestion list. 


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select Customer").FilterType(AutoCompleteFilterType.StartsWith).CaseSensitiveSearch(true).DataSource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Suppliers")).Fields(fields => fields.Text("ContactName"))
{% endhighlight %}


The following screenshot displays remote data binding:

![](Databinding_images/Databinding_img2.png)



## ImageField

ImageField property is used to map the specific field name of the given DataSource to render the icons/images for each suggestion list. The mapped field should contain the icon/image URL for each suggestion list.


{% highlight html %}
@model List<Countries>

@Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields=>fields.Text("country").Image("flag"))

{% endhighlight %}


For MVC, pass the DataSource through model. You can refer to the code example for defining the DataSource in the model.

{% highlight c# %}
public class Countries

    {

        public string country { get; set; }

        public string flag { get; set; }

    }

    public static class CountriesModel

    {

        public static List<Countries> source = new List<Countries>();

        public static List<Countries> setSource()

        {

            source.Add(new Countries {country="Afghanistan" ,flag=VirtualPathUtility.ToAbsolute("~/themes/sample/autocomplete/afghanistan.png")});

            source.Add(new Countries {country="Argentina" ,flag=VirtualPathUtility.ToAbsolute("~/themes/sample/autocomplete/argentina.png")});

            source.Add(new Countries {country="Australia" ,flag=VirtualPathUtility.ToAbsolute("~/themes/sample/autocomplete/Australia.png")}); 

            return source;

        }
{% endhighlight %}


The following screenshot displays the ImageField:

![](Databinding_images/Databinding_img3.png)


## ImageClass

ImageClass property is used to map the specific field name of the given DataSource to render the icons/images for each suggestion list. The mapped field should contain the CSS class names that define the icons/images for each suggestion list. You can customize the CSS class definitions for icons of each suggestion list based on the need.


{% highlight html %}
@model List<Countries>

@Html.EJMobile().AutoComplete("accmultivalue").DataSource(Model).Fields(fields=>fields.Text("country").Image("flag"))

{% endhighlight %}



{% highlight css %}




<style>

        .afghan {

        background-image: url("../themes/sample/autocomplete/afghanistan.png");

        background-position: center center;

        background-size: 30px 30px;

        }

        .argen {

        background-image: url("../themes/sample/autocomplete/argentina.png");

        background-position: center center;

       background-size: 30px 30px;

        }

        .aust {

        background-image: url("../themes/sample/autocomplete/australia.png") ;

        background-position: center center;

        background-size: 30px 30px;

        }

    </style>
{% endhighlight %}



For MVC, the class has to be referred in the model list.


{% highlight c# %}
    public class Countries

    {

        public string country { get; set; }

        public string flag { get; set; }

    }

    public static class CountriesModel

    {

        public static List<Countries> source = new List<Countries>();

        public static List<Countries> setSource()

        {

            source.Add(new Countries {country="Afghanistan" ,flag="afghan"});

            source.Add(new Countries {country="Argentina" ,flag="argen"});

            source.Add(new Countries {country="Australia" ,flag="aust"});

        }

        public static void clearSource()

        {

            source.Clear();

        }

    }
{% endhighlight %}


The following screenshot displays ImageClass:

![](Databinding_images/Databinding_img4.png)



