Storages
------------
Right now we will try to figure out what is storages and how to work with them. Storage it is... well, storage, the place where all report's object are stored. It can be filesytem, GIT, resource, HTTP server, FTP server. Certanly, you are familiar with some of them. CuteReport can use a lot of objects for report rendering, such as images and database files. Report files (templates) also stored somewhere. Usually you use your local filesystem to store all these objects as a file. But CuteReport is not limited only by filesystem. When you start CuteReport first time you will see "Storage settings" dialog:

![StorageSettings]


If you press on combobox on the top of the screen, you can see a list af all storages available. You need to select your primary storage and check "default". "Default" means storage for all url where schema is not indicated. 
For example, if you set default storage name as "Filesystem" then any objects with short url like "/objects/image.png" will be transformed to full url "file:/object/image.png". If you set "GIT" as default storage, then object "images/logo.png" will be transformed to "git:images/logo.png". Absolute or relative path is acceptable.
You can change these settings anytime in the main menu "Tools->Options->Storage"








[StorageSettings]:../images/storage_dialog.png
