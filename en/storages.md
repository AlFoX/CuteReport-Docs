Storages
======

Right now we will try to figure out what is storages and how to work with them. Storage it is... well, storage, the place where all report's object are stored. It can be filesytem, GIT, resource, HTTP server, FTP server. Certanly, you are familiar with some of them. CuteReport can use a lot of objects for report rendering, such as images and database files. Report files (templates) also stored somewhere. Usually you use your local filesystem to store all these objects as a file. But CuteReport is not limited by only filesystem. When you start CuteReport first time you will see "Storage settings" dialog:

![StorageSettings]


If you press on combobox on the top of the screen, you can see a list af all storages available. You need to select your primary storage and check "default". "Default" means storage for all url where schema is not indicated. 
For example, if you set default storage name as "Filesystem" then any objects with short url like "/objects/image.png" will be transformed to full url "file:/object/image.png". If you set "GIT" as default storage, then object "images/logo.png" will be transformed to "git:images/logo.png". Absolute or relative path is acceptable.
You can change these settings anytime in the main menu "Tools->Options->Storage". Storage can be global or report's local. global storages are used by CuteReport core. If report object has it's own assigned local storage than it will be used before global one.

FileSystem storage
----------

FileSystem is the most commonly used storage. It has only few options: "root folder" and "ask for rewrite". Root folder is the upper directory accessible to user. "Ask for rewrite" option is used to detect is it needed to show dialog for overwrite file if it's already exists while saving.

GIT storage
-------

It can be used for keeping all reports and theirs objects in local or remote GIT. Options:
* remote url: git repository url
* login, password: credentials to access git repository
* local path: local directory where git repo will be cloned in
* git binary: git console binary. CuteReport uses external git binary to oparate git repository, so it has to be defined
* "sync now" button: button for cloning or pulling data from remote repository

Resource storage
---------

All objects stored in this storage will be included to report's file while saving. 


All storages has it's own URL schema like: "git", "file", "res", "sql" so any file on these storages can be accessed using "git:objects/test.png", "res:/prefix/file1.jpg", "file:/home/user/file.bmp".


SQLStorage
-------
This storage is designed to make you easy to save and load report templates and report objects from SQL databases without writing any code in your application. Just provide info about database, table and field where reports or object are stored.


[StorageSettings]:../images/storage_dialog.png
