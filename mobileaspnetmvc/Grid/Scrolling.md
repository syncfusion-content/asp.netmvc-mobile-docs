---
layout: post
title: Scrolling| Grid | MobileAspNetMVC | Syncfusion
description: scrolling
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Scrolling

## Default

Scrolling is an important feature in Mobile Grid. It makes Grid more compatible with layout. You can enable scrolling in Grid by using AllowScrolling property in grid at grid initializes. In this following example, scrolling properties is used to adjust grid width and height of grid. Use the following code to enable scrolling feature in Mobile Grid. 

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/").Offline(true))

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("Freight").HeaderText("Freight").Add();

})

.AllowScrolling(true)

.ScrollOption(s=>s.Height(352)))


{% endhighlight %}


Result of above code snippet

![22](Scrolling_images/Scrolling_img1.png)


## Column scrolling 

Column scrolling is powerful technique in ejmGrid. It makes Grid more compatible with layout. It is very useful feature for Mobile Grid with more columns. By enabling “EnableColumnScrolling” property you can achieve column scrolling. 

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/").Offline(true))

.AllowScrolling(true)

.ScrollOption(s => s.EnableColumnScrolling(true).Height(352))

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Width(100).Add();

col.Field("CustomerID").HeaderText("Customer ID").Width(140).Add();

col.Field("EmployeeID").HeaderText("Employee ID").Width(140).Add();

col.Field("Freight").HeaderText("Freight").Width(100).Add();

}))

{% endhighlight %}


Execute the above code to render the following output.


![23](Scrolling_images/Scrolling_img2.png)




