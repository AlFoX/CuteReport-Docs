Report with Images
---------
In this chapter we will learn how to use Image object and FileSystem storage.<br>
Lets create new report, add new page, add Title band and Detail band. Nexts is creating FileSystem dataset. Go to "Datasets" tab, choose Standard::FileSystem and press it. Choose any directory that contains some pictures by pressing "Select dir..." button. Set "maxNumber" to 6. This is maximum records that dataset will contain. Disable flags: Directories, All Directories. Add filter: "*.jpg; *.png" or any other graphic format you have. Set "Path appearance" to "AbsolutePath", so we will be able to load picture using it's absolute path. Now press "Test it". As result you should see a list of 6 files or less with file format you set in your filter.

Now go to the Page Editor. Add Memo object to the Title, type there "Customer's pictures" and make text centered. For better appearance
change "backgroundBrush" for the Title. set "backgroundBrush::style" to "SolidPattern" and "backgroundBrush::color" to #688482. Now change text color. Click on the Memo and change property "textColor" to white. Well done!

Now we are starting to make image display. Set height of the Detail to 30mm. Add Image object to the right side of the Detail and change size to fit to the detail. set "sourceType" = "Dataset" and "source" = "file://[data."name"]". As you remember everything inside squre brackets will be identified as expression and will be replaced by expression result. So oour expression finaly will looks like "file://picture_path/picture.jpg". Well there is another very important thing: **if report loads any data in runtime, it MUST have storage assigned!**. This is done for security. In some cases you may not allow user to use any storage CuteReport has. So go to the "Reports" tab, and add "Standard::FileSystem" storage in the "Storage" tab. We have images path as absolute path, so clean up "Root folder" for this storage.

And the last step: Memo item that contains file's path. Add new Memo to the right side of the Detail band and type there: "[data."Name"]". Users of the Commercial edition can simply press on the button, that appears when you hover mouse over the Memo. 

Finally you repport template should looks like this:

![ImagesReport]


Now it's time to press "F5".




[ImagesReport]:../images/images_report.png
