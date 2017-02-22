---
layout: post
title: Scrolling Settings| Dialog | MobileAspNetMVC | Syncfusion
description: scrolling settings
platform: mobileaspnetmvc
control: Dialog
keywords: dialog, scrolling
documentation: ug
---

# Scrolling Settings

## Allow scrolling   

To enable  scrollingbehavior for the Dialog content. The default value is true.

{% tabs %}
        {% highlight html %}
@{

    @Html.EJMobile().Dialog("alertdlg").Title("Audi").LeftButtonCaption("Cancel").AllowScrolling(false).Content(

    @<div>

         It is a concept vehicle with Liquid Silver body colour, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)
         and 400 N·m (295.02 lbf·ft), diesel particulate filter and Bluetec emission control system, quattro permanent four-wheel drive system with Haldex clutch,
         Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
         MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.
    </div>)

}

<div style="text-align: center">

    @Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

</div>
         {% endhighlight %}

         {% highlight javascript %}
        



        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Scrolling-Settings_images/Scrolling-Settings_img1.png)





## EnableNativeScrolling

 To enable native (built-in browser) scrolling functionality of the devices when scrolling is allowed. The default value is false.

{% tabs %}
{% highlight html %}
        @Html.EJMobile().NavigationBar("header").Title("Dialog")

        <div id="content">
            @{

                @Html.EJMobile().Dialog("alertdlg").Title("Audi").LeftButtonCaption("Cancel").AllowScrolling(true).EnableNativeScrolling(true).Content(

                @<div>

                    It is a concept vehicle with Liquid Silver body colour, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)
                    and 400 N·m (295.02 lbf·ft), diesel particulate filter and Bluetec emission control system, quattro permanent four-wheel drive system with Haldex clutch,
                    Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
                    MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.
                </div>)

            }



            <div style="text-align: center">

                @Html.EJMobile().Button("btn1").Text("Click here to open dialog").ClientSideEvents(evt => { evt.TouchEnd("openAlertDialog"); })

            </div>


{% endhighlight %}

{% highlight javascript %}




        function openAlertDialog(args)

        {

            App.activePage.find("#alertdlg").ejmDialog("open");

        }
{% endhighlight %}
{% endtabs %}

The following screenshot displays the output.

![](Scrolling-Settings_images/Scrolling-Settings_img3.png)


