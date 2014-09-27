Label printing
=======
(__*commercial version only*__)


In this chapter we will see how to create report with columns using CuteReport. That can be useful to print labels or so. Let's create a simple report contains customer labels to print out on customer case folders. Below you can see this exaple:

![PageWOColumns]

And after rendering we have following:


![PageWOColumns_2]

As you can see there is a lot of wasted space on the right side, therefore a lot of wasted paper. To optimize the space we will set a number of columns that will fit all our labels. It can be done using __"columns"__ property of Page. Set it to "3" in the PropertyEditor on the right size of screen. Then press __"F5"__ to generate report.

![PageWOColumns_3]

There are 2 types of column filling: __"Vertical"__ and __"Horizontal"__ that can be set via __"fillDirection"__ Page's property. In the picture above you can see "Vertical" type that means any next label will be printer under the previous and so on while there is empty space exists in the column. When there is no space, report will create new column and start from the top. "Horizontal" type means every next label will be printed on the right of previous one while there is enought space on the right side of page. If there is no space, report will print next label on the next row as you can see below:

![PageWOColumns_4]

You can sent any type depending of your needs. Not all bands respect column setting. Some ignore it, like PageHeader, PageFooter. Some other have special property to adjust this behavior, like DetailHeader or DetailFooter. using this option you can design complex columned reports. One of sample of columned report with grouping you can see below:

![PageColumns_5]


[PageWOColumns]:../images/columns_1.png
[PageWOColumns_2]:../images/columns_2.png
[PageWOColumns_3]:../images/columns_3.png
[PageWOColumns_4]:../images/columns_4.png
[PageColumns_5]:../images/columns_5.png
