---
layout: post
title: Item-Specific-Settings
description: item specific settings
platform: mobileaspnetmvc
control: ListView
documentation: ug
---

# Item Specific Settings

In the ListView widget, the following numbered settings are available for easy customization of Items as per user demand. In MVC, the properties are accessed with the property named ‘Items’. Following are the detailed explanation.

_Item specific settings_
{% highlight html %}

<table>
<tr>
<td>
Settings</td><td>
Properties</td></tr>
<tr>
<td>
Ajax Post</td><td>
1. Href-This property can hold either the ID of an element or the name of the HTML page.* Option 1 - ID: The value should start with ‘#<ID>’* Option 2 - HTML: The value should be like ‘<HTML>.html’ or ‘<HTML>.htm’.2. EnableAjax-This property must be set to true when the second option for href property is provided as mentioned above. </td></tr>
<tr>
<td>
<br>Selection</td><td>
1. MultiSelection* EnableCheckMark-This property is used to make the ListView as check list for multiple selection of items.* Checked-This property is used to make any item in checked state in the initial loading itself.2. PreventSelection-This property is used to prevent selection while clicking on the list item.3. PersistSelection-This property is used to persist the selection in the list item even after touch end. (By default, the active state is removed once touch end happens)</td></tr>
<tr>
<td>
<br>Item Customization</td><td>
Text-This property is used to set the text for the list item.</td></tr>
<tr>
<td>
Key Value</td><td>
PrimaryKey-This property is used to relate parent child and also to expose that the list item has inner page navigation.</td></tr>
<tr>
<td>
Image Customization</td><td>
1. ImageClass-This property is used to define the class name of the image that is to be rendered along with the list item.2. ImageUrl-This property is used to define the URL of the image that is to be rendered along with the list item.</td></tr>
<tr>
<td>
<br>Child Customization</td><td>
1. Header Settings* ChildHeaderTitle-This property is used to set the title of the header rendered in the child page.* ChildHeaderBackButtonText-This property is used to set the text for the button available in the header that is rendered in the child page.2. ChildId-This property is used to set the ID for the child item.</td></tr>
<tr>
<td>
<br>Templating</td><td>
1. RenderTemplate-This property is used to decide whether to render the list item with template or with default UI.2. TemplateId-This property is used to define the ID of the template element.</td></tr>
<tr>
<td>
<br>Events</td><td>
1. TouchStart-This property is used to define the handler when touch start happens on a particular list item.2. TouchEnd-This property is used to define the handler when touch end happens on a particular list item.</td></tr>
</table>

{% endhighlight %}

