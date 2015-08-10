---
layout: post
title: Customize-menu-item-and-its-images
description: customize menu item and its images
platform: mobileaspnetmvc
control: Radial Menu
documentation: ug
---

# Customize menu item and its images

You can customize Radial Menu items by using imagepath, imageurl and text properties. The imagepath property is used to define the path corresponding to the rendermode it get renders. Imagename can be used to define the name of image. Refer to the folder name that is required to keep the images for the corresponding render modes.

1. Ios7 – Folder name for ios7 specific images
2. Android – Folder name for Android specific images
3. Windows – Folder name for Windows specific images

Alternatively you can use imageurl property to directly specify the url of the image for the items. Text property is used to specify the item text in windows mode.

 _Note: Imagepath and imagename properties can be used when you want to specify separate images for each render mode. Imageurl property is used when you want to provide common images for all render modes._

Refer to the following code example.
{% highlight html %}

    @Html.EJMobile().RadialMenu("radialmenu_sample").Items(item =>{

item.Add().ImagePath(Url.Content("http://js.syncfusion.com/UG/Mobile/Content/radial")).ImageName("social.png"));    

item.Add().ImagePath(Url.Content("http://js.syncfusion.com/UG/Mobile/Content/radial")).ImageName("music.png"));

item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial /ios7/light/direction.png"));

item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial /ios7/light/message.png"));

item.Add().ImageURL("http://js.syncfusion.com/UG/Mobile/Content/radial /ios7/light/browser.png"));

})

<script>

    function click(e) {

        $("#radialmenu_sample").ejmRadialMenu("menuHide");

    }

</script>

{% endhighlight %}



