---
layout: post
title: Initialize ejmGrid| Grid | MobileAspNetMVC | Syncfusion
description: initialize ejmgrid
platform: mobileaspnetmvc
control: Grid
documentation: ug
---

# Initialize ejmGrid

In this section, you can learn the Mobile Grid’s mandatory property to render a simple Grid. To initialize Grid, it needs two important properties. They are columns and its inner property field. Columns are used to define schema of grid and field is mapping name to data source.

{% highlight javascript %}

$("#MobileGrid").ejmGrid({

     columns: [

        { field: "OrderID" },

        { field: "CustomerID" },

        { field: "EmployeeID" }

     ]

});

{% endhighlight %}



Execute the above code to render the following output.



'![1](Initialize-ejmGrid_images/Initialize-ejmGrid_img1.png)



_Empty grid_

