---
layout: post
title: Item-Specific-Settings
description: item specific settings
platform: mobileaspnetmvc
control: Menu
documentation: ug
---

# Item Specific Settings

In Menu widget, the following settings are available for easy customization of each Menu item as per user demand. In MVC, these properties can be accessed with the property named ‘Items’. Following are the detailed explanations.

_Settings for easy customization_
{% highlight html %}

<table>
<tr>
<td>
Settings</td><td>
Properties</td></tr>
<tr>
<td>
Item Customization</td><td>
Text-This property is used to set the text for the list of items.</td></tr>
<tr>
<td>
Navigation</td><td>
Href-This property is used to define the URL of the page to be navigated while selecting the Menu item.</td></tr>
<tr>
<td>
iOS7 Specific Customization</td><td>
1. Theme-This property is used to define the theme of the button rendered in the Menu item.2. ButtonStyle-This property is used to define the style of the button rendered in the Menu item.3. ButtonColor-This property is used to define the color of the button rendered in the Menu item.<br></td></tr>
<tr>
<td>
Android Specific Customization</td><td>
ImageClass-This property is used to define the Css class name by using the image that can be rendered along with the Menu item.</td></tr>
<tr>
<td>
Templating</td><td>
1. RenderTemplate-This property is used to decide whether to render the Menu item with template or with default UI.2. TemplateId-This property is used to define the ID of the template element.<br></td></tr>
<tr>
<td>
Events</td><td>
1. TouchStart-This property is used to define the handler when touch start happens on a particular Menu item.2. TouchEnd-This property is used to define the handler when touch end happens on a particular Menu item.</td></tr>
</table>

{% endhighlight %}

