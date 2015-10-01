---
layout: post
title: Customize Contenttype and Text| Button | MobileAspNetMVC | Syncfusion
description: customize contenttype and text
platform: mobileaspnetmvc
control: Button
documentation: ug
---

# Customize ContentType and Text

## ContentType

You can make the **Button** appear as an image or text or combination of both. This property allows you to choose the **ContentType** of the **Button** in your application. By default, the **ContentType** of **Button** is set to ‘**text**’.

The possible values are

* Text

* Image

* Both

You can refer to the following code examples.
{% highlight html %}
@Html.EJMobile().Button("sample_button").Text("button").ContentType(ButtonContentType.Text)
{% endhighlight %}


{% include image.html url="Customize-Contenttype-and-Text_images/Customize-Contenttype-and-Text_img1.png" Caption="Button – ContentType"%}


## Text

This property allows you to specify the text to be appeared inside the **Button** using ‘**Text**’ property. 

You can refer to the following code examples.

{% highlight html %}

@Html.EJMobile().Button("sample_button").Text("button")



{% endhighlight %}

{% include image.html url="Customize-Contenttype-and-Text_images/Customize-Contenttype-and-Text_img2.png" Caption="Button – Text"%}

