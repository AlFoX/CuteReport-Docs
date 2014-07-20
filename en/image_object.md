Image object
--------
Image object is designed to represent any images in supported graphical formats. Currently supported formats: BMP	(Windows Bitmap), GIF	(Graphic Interchange Format), JPG	(Joint Photographic Experts Group), JPEG (Joint Photographic Experts Group), PNG	(Portable Network Graphics), PBM	(Portable Bitmap), PGM (Portable Graymap), PPM	(Portable Pixmap), XBM	X11 (Bitmap), XPM (X11 Pixmap).
Lets look closer to this object. Create new report, add new page, add Image item. There are some data sources for the Image available: Static, Storage, Dataset. Type of source defined in "sourceType" property.  Lets review each option:
* "Static" allows you to load Image from the file and keep loaded data inside the object.
