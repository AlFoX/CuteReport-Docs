Now we will create our second report and will learn how to use datasets. For that we will use test sqlite database named "business.db".
By first create new empty report by pressing "main menu -> Report -> New Report". Then go to the "Datasets" tab, click on dataset names combobox and select SQL. Now you have one SQL dataset in your report. Lets set correct parameters for the dataset. Click "File...". When "Open database file" dialog appears, make sure you have correct storage selected in the "Storage" combobox, locate database file named "business.db" and choose it. Now you should have field "Database:" filled with "file:dataset.db". Since we have no host, user and passowrd for this database we will skip these fields. Choose "SQLITE" driver in the "Available Drivers:" list and press "<<" to copy driver name to the field "Driver". Now we can connect to out test database. Lets write a simple SQL query to test it:

```sql
select * from customer
```

As a result you will have something like on the picture below:

![sqldataset_helper]

Click "Test it" button and table with fetched from database data will appear. If there is error exists you will see it in the bottom frame. Well done! Now you have dataset completed.

![sqldataset_data]


Go to the tab "Page" and create new page if not exists. There are some types of page possible. For now we will use "Standard Page" or "Extended page"(for commercial version). Click on combobox and select appropriate page type and then click on the button "Add new page" ![AddNewPageButton].





[AddNewPageButton]:../images/add_new_page_button.png
[sqldataset_helper]:../images/sqldataset_helper.png
[sqldataset_data]:../images/sqldataset_data.png


