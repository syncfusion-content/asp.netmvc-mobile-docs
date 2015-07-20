---
layout: post
title: Configure-Badge
description: configure badge
platform: mobileaspnetmvc
control: Tile
documentation: ug
---

## Configure Badge

The Badge property handles badge specific functionalities like enable or disable the badge and setting badge value for tile. The Text property isusedtoset the text instead of number for tile badge. The MaxValue and MinValue properties areusedto set the maximum and minimum badge value to a tile respectively. 

Refer to the following code example.

<div style="margin-top:45px;">

@Html.EJMobile().Header("head").Title("Tileview")

@Html.EJMobile().Tile("tile").ImageUrl("messaging.png").ImagePath(Url.Content("~/themes/sample/tileview")).Text("Messaging").Badge(badge => { badge.Enabled(true).MaxValue(80).MinValue(10).Value(88); })

</div>



The following screenshot illustrates the output of the above code.

{{ '![C:/Users/labuser/AppData/Roaming/Skype/My Skype Received Files/badgechanges.png](Configure-Badge_images/Configure-Badge_img1.png)' | markdownify }}
{:.image }


