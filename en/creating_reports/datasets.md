Datasets
=====

As it was mentioned before Dataset is the objects that contains structured data organized into rows(lines) which have one or more columns(fields). Dataset can fetch data from any source and privode common interface to this data. There are some datasets provided in the basic CuteReport edition: SQLDataset, CSVDataset, FilesystemDataset, ModelDataset. All of them fetch data from diferrent sources.

Datasets:
* __SQLDataset__: It provides interface to fetch data from SQL databases, It can work with any databases supported by Qt, ie that has Qt database driver. There are some setting to connect to a remote database (like mysql, postgresql) or to use database file (like sqlite)
* __CSVDataset__: It provides interface to data stored in a file and separated by comma or other defined symbol. It can load data from en external file every time when populated or load and cache data internally
* __FilesystemDataset__: it provides interface to fetch information from filesystem, and show files, directories and more less detailed info about them. There are some options: filtering, recursion level, max number of exposed records. It is usefull for making files or photo catalogs, etc.
* __ModelDataset__: it is used to export prepared data from custom application to report object. If you have widget like QTableView or QTableWidget or your custom filtered/sorted model you can easily print data stored in there.

Try to play with each dataset to understand how they work. You can see the populated dataset rows anytime by pressing "Test it" button. Data from dataset can be used in scriptable form in items. To get data from dataset where it's allowed you can use __[datasetname."fieldname"]__ or __[datasetname.getValue("fieldname")]__ form. First form is just shortening of the second one. Every short form replaced by full form internally before script execution.


Further we will see how to connect dataset to a band and to use data more detailed.
