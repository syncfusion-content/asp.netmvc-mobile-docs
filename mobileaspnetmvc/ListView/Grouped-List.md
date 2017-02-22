---
layout: post
title: grouped-list
description: grouped list
platform: js
control: ListView
documentation: ug
keywords: grouped
---

## Grouped list

Here, you can learn how ListView with items are grouped together using the grouplist feature in ListView.

{% highlight html %}

    <!--Add Header Element Here-->
 @Html.EJMobile().NavigationBar("header").Title("MailBox")

    <!--Add Listview Element Here-->
        @Html.EJMobile().ListView("listview").Items(items =>
   {
       items.Add().GroupTitle("Mailboxes");
       items.Add().Text("Inbox");
       items.Add().Text("VIP");

       items.Add().GroupTitle("Labels");
       items.Add().Text("Draft");
       items.Add().Text("Sent");
       items.Add().Text("Junk");
       items.Add().Text("Trash");
       items.Add().Text("All Mail");
       items.Add().Text("Mail");
   })

{% endhighlight %}

![](grouped-list_images\grouped-list_img1.png)

