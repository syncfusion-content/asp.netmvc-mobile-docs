---
layout: post
title: Customize Suggestion List| AutoComplete  | MobileAspNetMVC | Syncfusion
description: customize suggestion list
platform: mobileaspnetmvc
control: AutoComplete 
documentation: ug
keywords: count ,filter
---

# Customize suggestion list

## Items count

ItemsCount specifies the number of items to be displayed in the suggestion list. By default, the value for the property is “5”.


{% highlight html %}
@model List<Cars>

 @Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name")).ItemsCount(2)
{% endhighlight %}


The following screenshot displays items count:

![](Customize-suggestion-list_images/Customize-suggestion-list_img1.png)


## Filter type

FilterType property is used to filter and display the suggestion list based on your requirements. The possible values are, 

1. Startswith
2. Contains

By default, the value for the property is “contains”.


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name")).FilterType(AutoCompleteFilterType.StartsWith)
{% endhighlight %}


## Enable distinct

EnableDistinct property is used to hide or show the duplicate items from the suggestion list. By default, the value for the property is “false”.


{% highlight html %}
@model List<Cars>

@Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name")).EnableDistinct(true)
{% endhighlight %}


## Sorting

AllowSorting property enables the sorting operation for the suggestion list. When it is set to true, the suggestion list is displayed in the sorting order that can be given by using the “SortOrder” property.

The possible values are,

1. Ascending
2. Descending




{% highlight html %}
@model List<Cars>

        @Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name")).SortOrder(SortOrder.Descending).AllowSorting(true)
{% endhighlight %}


The following screenshot displays sorting:

![](Customize-suggestion-list_images/Customize-suggestion-list_img3.png)



## Empty result

ShowEmptyResultText property is used to show or hide the suggestion box when there is no suggestion available for the user query. By default, the value is “true”.

EmptyResultText property is used to customize the text that is displayed when no results appear in the suggestion list. By default, the value is “No Suggestions”.


{% highlight html %}
@model List<Cars>

        @Html.EJMobile().AutoComplete("autocomplete_sample").DataSource(Model).Fields(fields => fields.Text("name")).ShowEmptyResultText(true).EmptyResultText("No Values available")
{% endhighlight %}


The following screenshot displays empty result:

![](Customize-suggestion-list_images/Customize-suggestion-list_img4.png)



