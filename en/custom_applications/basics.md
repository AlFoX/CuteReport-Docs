# Basics


There are some important steps to use CuteReport in the custom application:
- add all necessary data to your project file (.pro);
- add deader files of CuteReport to your cpp file;
- craate and init report core;

__Project file__


Add next lines to your .pro file:
```
INCLUDEPATH += path_to_cutereport_headers
DEPENDPATH += $$INCLUDEPATH

LIBS += -Lpath_to_cutereport_shared_files -lCuteReport -lCuteReportWidgets
```

add cutereport header files to your code:
```cpp
#include "reportcore.h"
#include "reportinterface.h"
```

__Working with CuteReport using ReportCore__

Next is creating CuteReport::ReportCore instance and init it:
```cpp
    CuteReport::ReportCore * reportCore = new CuteReport::ReportCore();
```
There are some parameters you can pass to the constructor:
- _parent_: sets parent object to the cutereport instance. if it is set you should not care about cutereport instance deletion;
- _settings_: a pointer to QSetting object. You can use your project's settings to allow cutereport to save its settings and states to the file using [CuteReport] group. The settings in this file can provide some initial info to configure CuteReport. Instead of writing a lot of code to add instancess like storages to the report, you can use custom settings. We will review these setting later. If QSetting pointer is not specified CuteReport will create its own ini file.
- _interactive_: used to specify if report objects are static or can be changed. If you develop some console application that process report templates without changing report objects you can safe some resources by using "false". It is true by default;
- _initLogSystem_: determines if you need or no to see CuteReport's logs. True by default. It should be mentioned that log estinations and log levels can be configured separately.

Additionlly you can cpnnect some signals to detect report exporting and rendering:
```cpp
    connect(reportCore, SIGNAL(exportDone(QString,bool)), this, SLOT(slotExportDone(QString,bool)));
    connect(reportCore, SIGNAL(printingDone(QString,bool)), this, SLOT(slotPrintDone(QString,bool)));
```

Now when we have core created we can load an report template:
```cpp
CuteReport::ReportInterface * report = reportCore->loadReport("file:/path/myreport.qtrp");
```
In most cases you might want to see report preview, so lets create preview widget:
```cpp
    CuteReport::ReportPreview * preview = new CuteReport::ReportPreview(reportCore);
    preview->connectReport(report);
```
By passing report pointer to the preview widget you specify what report object preview should be represented.

Now we can start report rendering. There are some ways to do this.
First one by pressing button "Run" in the preview widget.
Second one to invoke ReportCore method _render(report)_.
Third one is to invoke Preview method run();
You can choose any way.

