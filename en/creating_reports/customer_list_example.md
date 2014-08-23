"Customer List" example
====

Now we will create our second report and will learn how to use datasets. For that we will use test sqlite database named "business.db".
By first create new empty report by pressing "main menu -> Report -> New Report". Then go to the "Datasets" tab, click on dataset names combobox and select SQL. Now you have one SQL dataset in your report. Lets set correct parameters for the dataset. Click "File...". When "Open database file" dialog appears, make sure you have correct storage selected in the "Storage" combobox, locate database file named "business.db" and choose it. Now you should have field "Database:" filled with "file:dataset.db". Since we have no host, user and passowrd for this database we will skip these fields. Choose "SQLITE" driver in the "Available Drivers:" list and press "<<" to copy driver name to the field "Driver". Now we can connect to out test database. Lets write a simple SQL query to test it:

```sql
select * from customer
```

As a result you will have something like on the picture below:

![sqldataset_helper]

Click "Test it" button and table with fetched from database data will appear. If there is error exists you will see it in the bottom frame. Well done! Now you have dataset completed.

![sqldataset_data]

Go to the tab "Page" and create new page if not exists. There are some types of page possible. For now we will use "Standard Page" or "Extended page"(for commercial version). Click on combobox and select appropriate page type and then click on the button "Add new page" ![AddNewPageButton]. Add "Title" band to the page, and set correct size by dragging mouse on blue handle or by setting correct size in the PropertyEditor. Now place "Memo" item to the center of the band and set correct geomery as well. Double click on the Memo and type "Customer List" and press "Ok". To make this text centered, click on "TextFlags" propery in the PropertyEditor and enable "AlignHCenter" flag. Next step is adding "Detail" band to the page and joining it to our customers dataset. To do that press on the Dataset and to make it active and type "data" to the band's property "dataset". "Data" is the name of our dataset. You can change it anytime by double-clicking on the dataset tab in the DatasetsEditor. Now it's time to add some some "Memo" items to the band: number, first name, second name, address, city, zip code. For make it easy to stick each other, you can enable magnets by pressing buttons on the top of PageEditor. If you want to change name of the objects and make it more understandable in the Object Inspector, go to PropertyEditor and change "objectName" to something like: memoFirstName, memoSecondName, memoAddress and go on. We don't use these names in this example, but it can be useful to you later. Next to add instructions to our Memos what to display. Go to the first one, double click on it and type "[_line]". As we discussed before "[string]" means expression and _line is internal variable represents current dataset row. Press "F5" and you will see how does it work. Return back to the PageEditor by clicking on "Pages" at the leftsize and fill memo with the customer's first name. Add text "[data."firstname"]" to this Memo. User of the CuteReport commercial edition can simply click on the button that appears on the right side of the Memo as you can see here:

![MemoDropDown]

Do the same for all other items and set correct dataset field to draw. Press "F5" and you should see something like this:

![CustomerList1]

If you don't have such result, you can load report CustomerList.qtrp from CuteReport package and figure out what you did wrong.



[AddNewPageButton]:../images/add_new_page_button.png
[sqldataset_helper]:../images/sqldataset_helper.png
[sqldataset_data]:../images/sqldataset_data.png
[MemoDropDown]:../images/memo_dropdown.png
[CustomerList1]:../images/customerlist_1.png

