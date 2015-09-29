---
layout: post
title: Column Selection| Grid | MobileAspNetMVC | Syncfusion
description: column selection
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Column Selection

By enabling “AllowColumnSelector”, you can hide the columns dynamically whenever needed. This feature is mostly useful when the available device width is not enough to display all the necessary columns. 

{% highlight html %}

@(Html.EJMobile().Grid<object>("MobileGrid")

.Datasource(d=>d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"))

.AllowPaging(true)
.AllowColumnSelector(true)

.Columns(col =>

{

col.Field("OrderID").HeaderText("Order ID").Add();

col.Field("CustomerID").HeaderText("Customer ID").Add();

col.Field("ShipCity").HeaderText("Ship City").Add();

}))

{% endhighlight %}


Execute the above code to render the following output.



![27](Column-Selection_images/Column-Selection_img1.png)


![28](Column-Selection_images/Column-Selection_img2.png)


![29](Column-Selection_images/Column-Selection_img3.png)



