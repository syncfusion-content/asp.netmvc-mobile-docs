---
layout: post
title: templating
description: templating
platform: mobileaspnetmvc
control: ListView
documentation: ug
keywords: template
---

## Templating

Internal Template

By using template support, you can customize the appearance of the individual list item or render the whole ListView by using a single template. Setting the TemplateID and renders the ListView with template item.

{% highlight html %}

<div class="sample-control template listview">
        <div id="appScroll">
            <ul data-role="ejmlistview" id="templatelist" data-ej-datasource="window.dbitem" data-ej-templateid="lvtemplate"></ul>
        </div>
    </div>
    <script id="lvtemplate" type="text/x-jsrender">
        <div class="cont-bg">
            <div class="profile {{>Class}}">
            </div>
            <div class="listrightdiv">
                <span class="templatetext">{{>Name}}</span> <span class="designationstyle">{{>Designation}}</span>
                <div class="aboutstyle">
                    {{>About}}
                </div>
            </div>
        </div>
   </script>


{% endhighlight %}



{% highlight js %}
For MVC Wrapper sample, create a model file for Data Binding. Add the following model code to a CS file and save it as ListView.cs.

public class ListTemplate
    {
        public string Name { get; set; }
        public string Designation { get; set; }
        public string Class { get; set; }
        public string About { get; set; }
    }
    public static class ListTemplateModal
    {
        public static List<ListTemplate> listTempSource = new List<ListTemplate>();
        public static List<ListTemplate> setListTempSource()
        {
            listTempSource.Add(new ListTemplate { Name = "Brooke", Designation = "HR Assistant", Class = "brooke", About = "Brooke provides administrative support to the HR office." });
            listTempSource.Add(new ListTemplate { Name = "Claire", Designation = "HR Manager", Class = "claire", About = "Claire is responsible for strategic HR planning and budget." });
            listTempSource.Add(new ListTemplate { Name = "Erik", Designation = "Training Specialist", Class = "erik", About = "Erik notifies attendees and manages follow up." });
            listTempSource.Add(new ListTemplate { Name = "Grace", Designation = "Development Manager", Class = "grace", About = "Grace maintains training plans to achive workforce skill." });
            listTempSource.Add(new ListTemplate { Name = "Jacob", Designation = "Recruitment Manager", Class = "jacob", About = "Jacob manages recruitment and prepares key staffing metrics." });
            return listTempSource;
        }
         public static void clearSource()
        {
            listTempSource.Clear();
        }


                public ActionResult template()
        {
            ListTemplateModal.clearSource();
            return PartialView(ListTemplateModal.setListTempSource());
        }

{% endhighlight %}



{% highlight css %}

 .sample-control.template .e-m-lv-item {
    height: 85px;
    width: 100%;
    padding: 4px 0px;
}

    .sample-control.template .e-m-lv-item .cont-bg {
        padding-top: 10px;
        padding-left: 5px;
    }

.sample-control.template .designationstyle {
    float: right;
    font-size: 12px;
    position: relative;
    right: 25px;
    padding-top: 5px;
}

.sample-control.template .aboutstyle {
    display: block;
    font-size: 14px;
    line-height: 20px;
    overflow: hidden;
    padding-left: 10px;
    padding-right: 5px;
    text-align: justify;
}

.sample-control.template .templatetext {
    font-weight: bolder;
    position: relative;
    font-size: 17px;
    margin-left: 10px;
}

.sample-control.template .listrightdiv {
    position: relative;
}

.sample-control.template .e-m-lv-active .listrightdiv {
    color: white;
}

.sample-control.template .e-m-lv-item .brooke {
    background-image: url('sampleimages/Employees/1.png');
}

.sample-control.template .e-m-lv-item .claire {
    background-image: url('sampleimages/Employees/2.png');
}

.sample-control.template .e-m-lv-item .erik {
    background-image: url('sampleimages/Employees/3.png');
}

.sample-control.template .e-m-lv-item .grace {
    background-image: url('sampleimages/Employees/4.png');
}

.sample-control.template .e-m-lv-item .jacob {
    background-image: url('sampleimages/Employees/5.png');
}

.sample-control.template .profile {
    background-repeat: no-repeat;
    background-size: 49px 48px;
    border: 1px solid #e5e5e5;
    float: left;
    height: 52px;
    position: relative;
    width: 50px;
}


{% endhighlight %}

![](templating_images\templating_img1.png)

