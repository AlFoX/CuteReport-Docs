Multi-page report
===


It is possible to create several design pages in the CuteReport. This feature is useful if report should contain different pages with different size, orientation, etc. In this case report engine will fully render first page and then second and so on. Total number of design page is not limited.
Let us look at the simple example with 2 pages where first one is title page and second one is report itself. We will use our previous example "Customer List". To add new page click on the button ![Multipage1] on the toolbar of the PageEditor. If there is some kind of pages you will see drop-down menu. Then choose page type you want by clicking it. New page will be added to the end. Move it to the begin by clicking ![Multipage2]. Since item cannot be placed direct on page, we will add __Overlay__ band first to the middle of the page. Now add Memo item to the band and type "Customer Report" in there. Render report and now it should look like:

![Multipage3]


[Multipage1]:../images/multipage_1.png
[Multipage2]:../images/multipage_2.png
[Multipage3]:../images/multipage_3.png
