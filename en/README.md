Introduction
===

**CuteReport** is a free report solutions based on Qt4 framework and it can be easily used with any Qt application. Generally CuteReport consists of two parts: core library and template designer. Both are totally modular and theirs functionality can be simply extended by writing additional modules. It's totally abstact of used data and can use as storage: file system, database, version control systems, etc.
The projects's goal is to provide powerfull, but yet simple to use for unexperienced user and report designers.


**Key Features:**

* A number of data sources: SQL database, Text, FileSystem,  information, external data model (QAbstractItemModel);
* Various types of storages to keep report templates and report's objects like picture, etc: Filesystem, GIT, SQL database, embedded storage;
* Plain text or HTML support;
* Variety of Drawing elements to construct great looking reports: text (Memo), Image, Barcode, Arc, Chart, Chord, Ellipse, Line, Pie, Rectangle;
* Picture sources: static, dataset, storage
* Unlimited number of details within one report;
* Report Title and Summary;
* Page Headers and Footers;
* Elements grouping;
* Aggregate functions: count, min, max, avg, sum;
* Plugin system for supporting to extend all functionality;
* Parameters that can be passed from a cutom application;
* Entire application full featured scripting engine to manage any aspect of the report rendering;
* Supported meassure units: Millimeters and Inches;
* Standalone WYSIWYG designer with ability to extend any functionality using custom plugins;
* Some preinstalled Designer plugins: ReportProperty editor, Page editor, Script editor, Dataset editor, Preview;
* Crossplatform;


**Distributions:**

CuteReport is destributed in 2 forms:

* Under GNU/GPLv3 license to help to the opensurce developers add reporting functionality to theirs opensoource projects. Core Library is provided under LGPLv2 and can be dynamicaly linked to proprietary products. CuteReport Designer is under GPLv3 thought and can not be compiled in to proprietary products. Read GPL/LGPLv2 license description for more information
* Under commercial license to provide high level support and high level bug fixing and feature implementing priority. Also commercial package provides some CuteReport extensions that opensource version dosn't have. In this documentation such features marked as "Commercial version only";
