Custom application example
====

Now let's do some coding. To add CuteReport library to your application you can do something like this:
```cpp
#include "reportcore.h"

/* create reportcore instance */
CuteReport::ReportCore * reportCore = new CuteReport::ReportCore(0 ,0, false);

/* create report preview widget */
CuteReport::ReportPreview * preview = new CuteReport::ReportPreview(parentWidget);

/* assign report core to our preview */
preview->setReportCore(reportCore);

/* loading report template from file and creating of report object */
CuteReport::ReportInterface * reportObject = reportCore->loadReport("git:report.qtrp");

/* connect created report object to the preview */
preview->connectReport(reportObject);

/* show preview widget */
preview->show();

/* start report renderning */
preview->run();
```

Usually you need only one reportCore instance in your application. Any number of Preview widget can be assigned to the core.
