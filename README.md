Designer
====


CuteReport solution comes with a standalone designer which helps to manage CuteReport's templates. CuteDesigner itself has only few functions and provides API to support modules. Modules are used to provide and extend all designer's functionality. Modules can provide (gui-modules) or do not provide (nongui-modules) user interface elements. Some of the basic gui modules are: ReportEditor, PageEditor, ScriptEditor, DatasetEditor, and Preview. Each module provides its own functionality and does not depend on the others. Also any module can be replaced by another with extended functionality.
 
ReportEditor module
-----

ReportEditor is the first module in designer's tab bar. It is responsible for managing report objects and providing such operations as: load, save, create, delete. These operations are presented by GUI elements on ReportEditor's widget and are exported to the application's main menu. This module can support a number of open reports at the same time and switch between open reports. Also it manages embedded report's modules like: Storage, Renderer, and Printer. If there are not any joined embedded modules then the global one will be used. If you need special options for Storage, Renderer, or Printer, you should join the module you need to the report object and set the needed options. ReportEditor has a table with global report's variables and their values. These values are used in rendering the report and can be set manually in this table or by software.

[ReportEditorImage]

Key to ReportEditor features:
* main menu
* modules bar
* ReportEditor tab
* report variables
* embedded report modules

PageEditor module
-----

PageEditor module is responsible for making the report page template. It provides tools for managing page bands and items. To activate PageEditor press the "Page" tab on the modules bar. Pages bar shows the tab with all created pages. You can use it for switching between pages (mouse click) or for renaming the current page (mouse double-click). There are 3 buttons on the page's toolbar: create new page, delete current page, and clone current page. Next go 2 buttons with drop-down lists, first one for bands, second one for items. After that you can see some buttons for changing zoom and next 4 buttons for enabling/disabling page magnets. If magnets are enabled, the mouse pointer will stick to the other item's borders with the coordinate that is close to the cursor coordinate. Sticking factor can be changed in the page property "magnetRate". Magnet may not always work as you want, so sometimes it's better to disable them. On the right side of the page widget you can see ObjectInspector. All items that page contains are represented there as a tree. You can switch between items using ObjectInspector or by clicking the item on the workspace(#12). PropertyEditor is the next area. There are all the editable properties that the page has. By pressing the property item you can see a short property description (#11). The Workspace (#12) shows the entire page template. You can add a new band of items using drag-n-drop from drop-down list(#4, #5) to the page on the workspace. Almost all items can be placed only on a band, and bands can be placed only on the page directly. Press the "Delete" button to delete the band or item with all their children items. There is no Undo function yet, so be careful.

[PageEditorImage]

Key to PageEditor features:

* modules bar with PageEditor activated
* pages bar
* buttons: "new page", "remove page"
* drop-down list of bands
* drop-down list of items
* zooming buttons
* magnets enabling/disabling
* rise/lower item
* object inspector
* property editor
* property description
* workspace

ScriptEditor module
-----

You can switch to ScriptEditor by pressing the "Script" button on the module bar. Script editor is a pretty simple module and contains an editor with syntax highlighting and "Validate" button. Validation checks only the syntax correctness of your script and doesn't actually run the script. So even if your script passed validation, it still may contain runtime errors. Usually you can see all errors by pressing the green button on the left bottom of the Designer window. If there are errors in the script, the button becomes red. ScriptEditor uses javascript as scripting language.

[ScriptEditorImage]

DatasetEditor module
-----

You can switch to ScriptEditor by pressing the "Dataset" button on the module bar (#1). All created datasets of the current report are shown on the datasets bar (#2). Using this bar you can switch between datasets (mouse click) or rename the current dataset (mouse double-click). For creating a new dataset, press combobox #3 and choose the dataset type you want. Basic distribution provides 3 datasets: CSV dataset, SQL dataset and FileSystem Dataset. Each dataset is described below. To delete the current dataset, press button #3. There is no Undo function implemented yet, so be careful while deleting. When you have set all the options for the created dataset, you can press the "Test it" button (#5). All datasets have a common interface and provide data as a table. Each dataset has its own configuration widget (#6).


[DatasetEditorImage]

Key to DatasetEditor features:

* modules bar with DatasetEditor activated
* datasets bar
* new dataset combobox
* delete current dataset
* test dataset
* dataset helper
 
Preview module
------

Preview module task is to display rendered reports. There are some button groups to help you. First is the button for rendering current report template (#2). Every time you need to render or rerender your report this button will be helpful. Or you can use: Main Menu -> Service -> Render or just press F5. If your report need some time for rendering, process dialog will appears. To stop current rendering press this button again (or press F5). After report is rendered you can change zoom by using buttons: fit to page, fit width, zoom in, zoom out (#3, #4) or you can set any zoom you need in percent widget. To switch current page use buttons: First page, Previous Page, Next Page, Last Page or set page number direct in page number widget. Finally you can print rendered report (#7) or export it to the file(#6).

[PreviewImage]

Key to Preview features:

* modules bar with Preview activated
* Render report button
* fit page to view button group
* zooming button group
* page navigation
* export to file
* print

