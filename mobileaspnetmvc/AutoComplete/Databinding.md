---
layout: post
title: Databinding| AutoComplete  | MobileAspNetMVC | Syncfusion
description: databinding
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
keywords: databinding, local, remote
---

# Databinding

## Local databinding

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

            source.Add(new Cars { name = "Audi S7" });
            
             source.Add(new Cars { name = "BMW 7' });

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

![](data-binding_images\local-databinding_img1.png)



## Remote databinding

Mapper property is used to specify the remote URL of the DataSource for the suggestion list. 


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").WatermarkText("Select Customer").FilterType(AutoCompleteFilterType.StartsWith).CaseSensitiveSearch(true).DataSource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Suppliers")).Fields(fields => fields.Text("ContactName"))
{% endhighlight %}


The following screenshot displays remote data binding:

![](data-binding_images\remote-databinding_img1.png)



