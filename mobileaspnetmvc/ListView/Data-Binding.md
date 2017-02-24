---
layout: post
title: data-binding
description: data binding
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: listview, databinding
---

## Data binding

### Local data binding

The local data can be an array of JSON objects which is assigned for the ListView widget’s datasource property. Refer the below example.

{% highlight html %}

   @Html.EJMobile().ListView("locallistbox").DataSource(Model).Fields(f => { f.Text("texts"); });

{% endhighlight %}
For MVC Wrapper sample, create a model file for Data Binding. Add the following model code to a CS file and save it as ListLocalData.cs.

{% highlight js %}
        public ActionResult databindinglocal()
        {
            ListLocalDataModal.clearSource();
            return PartialView(ListLocalDataModal.setListSource());
        }


 public class ListLocalData
    {
        public string texts { get; set; }
    }
    public static class ListLocalDataModal
    {
        public static List<ListLocalData> listSource = new List<ListLocalData>();
        public static List<ListLocalData> setListSource()
        {
            listSource.Add(new ListLocalData { texts = "Discover Music"});
            listSource.Add(new ListLocalData { texts = "Sales and Events" });
            listSource.Add(new ListLocalData { texts = "Categories });
            listSource.Add(new ListLocalData { texts = "MP3 Albums"});
            listSource.Add(new ListLocalData { texts = "More in Music" });
            return listSource;
        }
        public static void clearSource()
        {
            listSource.Clear();
        }
    }

{% endhighlight %}

![](data-binding_images\data-binding_img1.png)

### Remote data binding

The ListView control also provides support for Remote data binding. Here the remote data is placed in Web service and you can render the list items from the web service using Service URL. The data is in JSONformat.

{% highlight html %}

 @Html.EJMobile().ListView("remotelistbox").DataSource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders")).Fields(f => { f.Text("ShipCity"); }).ItemsCount(10)


{% endhighlight %}


![](data-binding_images\data-binding_img2.png)

