ReportEditor module
---

ReportEditor is the first module in designer's tab bar. It is responsible for managing report objects and providing such operations as: load, save, create, delete. These operations are presented by GUI elements on ReportEditor's widget and are exported to the application's main menu. This module can support a number of open reports at the same time and switch between open reports. Also it manages embedded report's modules like: Storage, Renderer, and Printer. If there are not any joined embedded modules then the global one will be used. If you need special options for Storage, Renderer, or Printer, you should join the module you need to the report object and set the needed options. ReportEditor has a table with global report's variables and their values. These values are used in rendering the report and can be set manually in this table or by software.

![Report Editor image][ReportEditorImage]

**Key to ReportEditor features:**
* main menu
* modules bar
* ReportEditor tab
* report variables
* embedded report modules

[ReportEditorImage]:images/Designer_reportEditor_withLabels.png
