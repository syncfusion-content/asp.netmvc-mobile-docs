---
layout: post
title: Image-Support
description: image support
platform: mobileaspnetmvc
control: Form Controls
documentation: ug
---

# Image Support

ImageClass

In your application, you can include image inside the Button. In that case, you can use ImageClass for Button control where you can specify the image to be displayed in the Button. Ensure that you need to set the ContentType to ‘Image’. 

You can refer the following code examples.



    <!--In head section-->

<style>

     .image {

            background-image: url("silverlight.jpg");

        }

</style>



    <!--In body section-->

@Html.EJMobile().Button("sample_button").ContentType(ButtonContentType.Image).ImageClass("image")





{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML2abcd1f9.PNG](Image-Support_images/Image-Support_img1.png)' | markdownify }}
{:.image }


ImagePosition

You can also set the position of the image in the Button. ImagePosition property allows you to specify the position of the image in your Button control. You can set the position of the image in the Button either after the text or before text by setting the image position to ‘rRght’ or ‘Left’ respectively.

By default this property is set to ‘Left’.

You can refer to the following code examples.



@Html.EJMobile().Button("sample_button").ContentType(ButtonContentType.Both).ImageClass("image").Text("button").ImagePosition(ButtonImagePosition.Left)





{{ '![C:/Users/deepal/AppData/Local/Temp/SNAGHTML2abf8235.PNG](Image-Support_images/Image-Support_img2.png)' | markdownify }}
{:.image }


