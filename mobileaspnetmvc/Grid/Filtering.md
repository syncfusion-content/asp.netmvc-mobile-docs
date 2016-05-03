---
layout: post
title: Filtering| Grid | MobileAspNetMVC | Syncfusion
description: filtering
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Filtering

Filtering behavior is used to filter particular or related records in Mobile Grid to review details of records. To enable filtering behavior in Mobile Grid you need to add AllowFiltering property at grid initialize. Filter Bar filtering feature is available in Mobile Grid. 

## Filter Bar

Filter bar is the filtering type available in Mobile Grid. It is otherwise called as text filtering because filter bar working is based on text boxes. Through this you can filter records. Filter bar contains expression to filter records. They are based on type of column. Refer the following table for expression usage

Filter Bar Record Table

<table>
<tr>
<td rowspan = "4">
Numeric column</td><td>
> value</td><td rowspan = "4">
To filter numeric column. You can use these expressions.</td></tr>
<tr>
<td>
< value</td></tr>
<tr>
<td>
= value</td></tr>
<tr>
<td>
!= value</td></tr>
<tr>
<td rowspan = "3">
String</td><td>
%value<br>(Starts with)</td><td rowspan = "3">
By default , string filtering works starts with operator</td></tr>
<tr>
<td>
value%<br>(Ends with)</td></tr>
<tr>
<td>
%value%<br>(Contains)</td></tr>
<tr>
<td>
Date</td><td>
Equal</td><td>
By default, date filter bar matches records with same date value</td></tr>
<tr>
<td>
Boolean</td><td>
Equal</td><td>
Boolean filter bar works with either true or false.</td></tr>
</table>


 Refer the following code example for filter bar

{% highlight html %}
 
@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource((IEnumerable<object>)ViewBag.datasource)

.AllowFiltering())

{% endhighlight %}

{% highlight c# %}

namespace MVCSampleBrowser.Controllers

{

public partial class GridController : Controller

{

public ActionResult GridView()

{

var DataSource = OrderRepository.GetAllRecords();

ViewBag.datasource = DataSource;

return View();

}



}

}

{% endhighlight %}

Execute the above code to render the following output.


![18](Filtering_images/Filtering_img1.png)


_Default Filtering_


## Filter operators

ejmGrid uses filter operators from DataManager that is used at the time of filtering. Here you can learn about filter operators and its usage categories. Filter operators denotes filtering type.

Filter Operators Table

<table>
<tr>
<th>
Column type</th><th>
Filter operators</th></tr>
<tr>
<td>
Number</td><td>
ej.FilterOperators.greaterThanej.FilterOperators.greaterThanOrEqualej.FilterOperators.lessThanej.FilterOperators.lessThanOrEqualej.FilterOperators.equal</td></tr>
<tr>
<td>
String</td><td>
ej.FilterOperators.startsWithej.FilterOperators.endsWithej.FilterOperators.containsej.FilterOperators.equalej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Boolean</td><td>
ej.FilterOperators.equalej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Date</td><td>
ej.FilterOperators.greaterThanej.FilterOperators.greaterThanOrEqualej.FilterOperators.lessThanej.FilterOperators.lessThanOrEqualej.FilterOperators.equal</td></tr>
</table>

