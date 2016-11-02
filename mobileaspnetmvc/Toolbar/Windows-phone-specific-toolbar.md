---
layout: post
title: Windows phone specific toolbar| Toolbar | MobileAspNetMVC | Syncfusion
description: windows phone specific toolbar
platform: mobileaspnetmvc
control: Toolbar
documentation: ug
---

# Windows phone specific toolbar

In windows phone mode, when the number of toolbar items is more than 4, then the remaining items is rendered inside a menu container. And an overflow icon is added with toolbar to display the menu container.

Refer to the following code example.

{% highlight html %}

@Html.EJMobile().NavigationBar("toolbar_sample").Mode(NavBarMode.Toolbar).RenderMode(RenderMode.Windows).Items(item =>

   {

      item.Add().IconName("add");
      item.Add().IconName("cut");
      item.Add().IconName("copy");
      item.Add().IconName("save");
      item.Add().IconName("search");

   })

{% endhighlight %}

 The following screenshot illustrates the output of the above code.

![](Windows-phone-specific-toolbar_images/Windows-phone-specific-toolbar_img1.png)



