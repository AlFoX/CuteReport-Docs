Image object
=====

Image object is designed to represent any images in supported graphical formats. Currently supported formats: BMP	(Windows Bitmap), GIF	(Graphic Interchange Format), JPG	(Joint Photographic Experts Group), JPEG (Joint Photographic Experts Group), PNG	(Portable Network Graphics), PBM	(Portable Bitmap), PGM (Portable Graymap), PPM	(Portable Pixmap), XBM	X11 (Bitmap), XPM (X11 Pixmap).
Lets look closer to this object. Create new report, add new page, add Image item. There are some data sources for the Image available: Static, Storage, Dataset. Type of source defined in **sourceType** property.  Lets review each option:
* **Static** allows you to load Image from the file and keep loaded data inside the object. File must be loaded manualy by pressing "image" property in the PropertyEditor.
* **Storage** allows you to load file in runtime. Image propery "source" must be defined and it should be file url. If url schema is not defined, url schema from default storage will be added. Property "source" can contain normal text url and/or expression. For example , if source = "[data."filename"]" it will take file name from a database and will load this file from a storage.
* **Dataset** allows you to load file from dataset blob. Image propery "source" must be defined the same way as for "Storage".

Some of the other properties. if **keepAspectRatio** is set to "true", image when scalled will always keep original aspect ratio. If **center** is set to true, image when scalled with keeping aspect ration will always be centered.
