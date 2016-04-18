---
layout: post
title: Data binding| Grid | MobileAspNetMVC | Syncfusion
description: data binding
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Data binding

## Local data

Mobile Grid data source can be set in server-side through ASP.NET MVC by using ViewBag.

To achieve this refer the following code example.
{% tabs %}
{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource((IEnumerable<object>)ViewBag.datasource)

.Columns(col =>

{

col.Field("FirstName").HeaderText("First Name").Add();

col.Field("LastName").HeaderText("Last Name").Add();

col.Field("Email").HeaderText("Email").Add();

}))

{% endhighlight %}

{% highlight c# %}

namespace MVCSampleBrowser.Controllers.Grid

{

public class GridController : ApplicationController

{



public class Person

{

public string FirstName { get; set; }

public string LastName { get; set; }

public string Email { get; set; }

}



public ActionResult Default()

{

List<Person> Persons = new List<Person>();

Persons.Add(new Person() { FirstName = "John", LastName = "Beckett", Email = "john@syncfusion.com" });

Persons.Add(new Person() { FirstName = "Ben", LastName = "Beckett", Email = "ben@syncfusion.com" });

Persons.Add(new Person() { FirstName = "Andrew", LastName = "Beckett", Email = "andrew@syncfusion.com" });

ViewBag.datasource = Persons;

return View();

}

}

}

{% endhighlight %}
{% endtabs %}

Execute the above code to render the following output.

![2](Data-binding_images/Data-binding_img1.png)


## Remotedata

### oData binding

oData is standardized protocol for creating and consuming data. You can able to retrieve data from oData service using DataManager. Here is an example of remote Data binding using oData service.

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders")

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("Freight").HeaderText("Freight").Add();

}))

{% endhighlight %}

Execute the above code to render the following output.


![3](Data-binding_images/Data-binding_img2.png)



Note: For information about DataManager with Mobie Grid check DataAdaptors concept.


## Loadatonce

Through this load at once technique, you can able to load all remote data from server to grid and process records in client side. You can check load at once with grid.

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource(d=>d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/")
.Offline(true))

.AllowPaging(true)

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("ShipCity").HeaderText("Ship City").Add();

}))


{% endhighlight %}

Execute the above code to render the following output.


![4](Data-binding_images/Data-binding_img4.png)


## Cross domain

ejmGrid can use CrossDomain data service with help of data manager. Following configuration is to configure in client side. You need to configure server to retrieve data from server code. For server configuration, you can refer this link ([https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS)). Here you can learn how to use or retrieve cross domain data from Grid.

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource(d => d.URL("http://mvc.syncfusion.com/UGService/api/Orders")
.CrossDomain(true).Offline(true))

.AllowPaging(true)

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("ShipCity").HeaderText("Ship City").Add();

}))


{% endhighlight %}

Execute the above code to render the following output.


![6](Data-binding_images/Data-binding_img5.png)


## Load on Demand 

Load on demand is a powerful technique that is used to reduce bandwidth size of consuming data. In ejGrid, you have support to use load on demand. In the following example, oDataservice is used. At load time, it retrieves required data from service, only for the visible page and not for all records. And when you move to another page, it loads for current page. You no need to configure Grid to enable load on demand, since load on demand is enabled by default in Grid. The following code example illustrates you on how load on demand works with MobileGrid.

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/")

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("Freight").HeaderText("Freight").Add();

})

.AllowPaging(true)) 

{% endhighlight %}


Execute the above code to render the following output.

![6](Data-binding_images/Data-binding_img6.png)


## Refresh data source

ejmGrid contains a feature to refresh datasource dynamically after Grid initialization. It is useful to refresh grid data source.

{% tabs %}
{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource((IEnumerable<object>)ViewBag.datasource)

.Columns(col =>

{

col.Field("FirstName").HeaderText("First Name").Add();

col.Field("LastName").HeaderText("Last Name").Add();

col.Field("Email").HeaderText("Email").Add();

}))

@Html.EJMobile().Button("Button").Text("Refresh").ClientSideEvents(c => c.TouchEnd("RefreshData")) ()

{% endhighlight %}

{% highlight javascript %}




<script type="text/javascript">

window.newData = [

{ FirstName: "Mike", LastName: "Tiko", Email: "mike@syncfusion.com" },

{ FirstName: "Robin", LastName: "Kole", Email: "robin@syncfusion.com" },

{ FirstName: "Keth", LastName: "Rover", Email: "keth@syncfusion.com" }

];



function RefreshData() {

$("#MobileGrid").ejmGrid({ dataSource: newData });

}

</script>

{% endhighlight %}

{% highlight c# %}

namespace MVCSampleBrowser.Controllers.Grid

{

public class GridController : Controller

{

public class Person

{

public string FirstName { get; set; }

public string LastName { get; set; }

public string Email { get; set; }

}



public ActionResult GridView()

{

List<Person> Persons = new List<Person>();

Persons.Add(new Person() { FirstName = "John", LastName = "Beckett", Email = "john@syncfusion.com" });

Persons.Add(new Person() { FirstName = "Ben", LastName = "Beckett", Email = "ben@syncfusion.com" });

Persons.Add(new Person() { FirstName = "Andrew", LastName = "Beckett", Email = "andrew@syncfusion.com" });

ViewBag.datasource = Persons;

return View();

}



}

}

{% endhighlight %}
{% endtabs %}

![7](Data-binding_images/Data-binding_img7.png)



## Supported DataTypes

ejmGrid supports data types in JavaScript such as string, number, datetime and Boolean. By default, ejmGrid reads datatypes from Mobile Grid Datasource. Grid uses these DataTypes for filtering and other operations. You can also customize these DataTypes through column property type. It overrides default data type reading. For example refer the following code.

{% highlight javascript %}

<script id="table1" type="text/template" >

<table>

<thead>

<tr>

<th>Laptop

</th>

<th>Model

</th>

<th>Price

</th>

<th>OS

</th>

<th>RAM

</th>

<th>ScreenSize

</th>

</tr>

</thead>

<tbody>

<tr>

<td>Dell Vostro</td>

<td>2520</td>

<td>39990</td>

<td>Windows 8</td>

<td>4GB</td>

<td>15.6</td>

</tr>

<tr>

<td>HP Pavilion Sleekbook</td>

<td>14-B104AU</td>

<td>22800</td>

<td>Windows 8</td>

<td>2GB</td>

<td>14</td>

</tr>

<tr>

<td>Sony Vaio</td>

<td>E14A15</td>

<td>42500</td>

<td>Windows 7 Home Premium</td>

<td>4GB DDR3 RAM</td>

<td>14</td>

</tr>

<tr>

<td>Lenovo</td>

<td>Yoga 13</td>

<td>57000</td>

<td>Windows 8 RT</td>

<td>2GB DDR3 RAM</td>

<td>11.6</td>

</tr>

<tr>

<td>Toshiba</td>

<td>L850-Y3110</td>

<td>57700</td>

<td>Windows 8 SL</td>

<td>8GB DDR3 RAM</td>

<td>15.6</td>

</tr>

</tbody>

</table>

</script>

{% endhighlight %}

{% highlight html %}

@(Html.EJMobile().Grid<object>("Grid")

.Datasource(ds => { ds.Table("#table1"); })

.Columns(col =>

{

col.Field("Laptop").HeaderText("Laptop Brands").Add();

col.Field("Model").HeaderText("Model").Add();

col.Field("Price").HeaderText("Price").TextAlign(TextAlign.Right).Width(90).Add();



}))

{% endhighlight %}

Execute the above code to render the following output.


![8](Data-binding_images/Data-binding_img8.png)


_HTML binding_


## oData Adaptor

Now a days oData is most useful technique in consuming data. You can use oData protocol through Data Manger’s OData adaptor. Refer the following code to use oData adaptor with Grid.

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource("http://mvc.syncfusion.com/Services/Northwnd.svc/Products/")

.Columns(col =>

{

col.Field("ProductID").HeaderText("Product ID").Add();

col.Field("ProductName").HeaderText("Product Name").Add();

col.Field("UnitPrice").HeaderText("Unit Price").Add();

}))


{% endhighlight %}

Execute the above code to render the following output.

![11](Data-binding_images/Data-binding_img9.png)





