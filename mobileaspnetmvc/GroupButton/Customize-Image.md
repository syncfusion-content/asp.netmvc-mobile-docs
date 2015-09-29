---
layout: post
title: Customize Image| Group Button | MobileAspNetMVC | Syncfusion
description: customize image
platform: mobileaspnetmvc
control: Group Button
documentation: ug
---

# Customize Image

## ImageClass

By using this property, you can add specific style to each Group Button item. When a string value is given to ‘ImageClass’ attribute, it adds as a class in the particular item. You can add an image or style by using that class. To achieve this, you can add ‘ImageClass’ attribute to every item.

{% highlight html %}

@Html.EJMobile().GroupButton("groupbutton_sample").GroupButtonType(GroupButtonType.radio).

Name("options").Buttons(button =>

{

button.Add().Text("ipad").ImageClass("apple");

button.Add().Text("ipod").ImageClass("apple");

button.Add().Text("iphone").ImageClass("apple");

})

<style>

.apple {

background: url("apple.png") no-repeat;

background-position: 6px 50%;

background-repeat: no-repeat;

background-size: 20px 20px;

position: relative;

text-indent: 20px;

}

</style>

{% endhighlight %}

The following screenshot displays the Image Class:

![](Customize-Image_images/Customize-Image_img1.png)


## ImageUrl

ImageUrl property takes the image given in ‘Imageurl’ attribute and displays the image before the text in Group Button item.

{% highlight html %}

@Html.EJMobile().GroupButton("groupbutton_sample").GroupButtonType(GroupButtonType.radio).

Name("options").Buttons(button =>

{

button.Add().Text("ipad").ImageUrl("ipad.png");

button.Add().Text("ipod").ImageUrl("ipod.png");

button.Add().Text("iphone").ImageUrl("iphone.png");

})

{% endhighlight %}

The following screenshot displays the Image URL:

![C:/Users/vincentxavier/Desktop/Work/Documentation/Complete Doc/Groupbtton/images/ios7_4.png](Customize-Image_images/Customize-Image_img2.png)



