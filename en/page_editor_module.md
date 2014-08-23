Page Editor module
---

PageEditor module is responsible for making the report page template. It provides tools for managing page bands and items. To activate PageEditor press the "Page" tab on the modules bar. Pages bar shows the tab with all created pages. You can use it for switching between pages (mouse click) or for renaming the current page (mouse double-click). There are 3 buttons on the page's toolbar: create new page, delete current page, and clone current page. Next go 2 buttons with drop-down lists, first one for bands, second one for items. After that you can see some buttons for changing zoom and next 4 buttons for enabling/disabling page magnets. If magnets are enabled, the mouse pointer will stick to the other item's borders with the coordinate that is close to the cursor coordinate. Sticking factor can be changed in the page property "magnetRate". Magnet may not always work as you want, so sometimes it's better to disable them. On the right side of the page widget you can see ObjectInspector. All items that page contains are represented there as a tree. You can switch between items using ObjectInspector or by clicking the item on the workspace(#12). PropertyEditor is the next area. There are all the editable properties that the page has. By pressing the property item you can see a short property description (#11). The Workspace (#12) shows the entire page template. You can add a new band of items using drag-n-drop from drop-down list(#4, #5) to the page on the workspace. Almost all items can be placed only on a band, and bands can be placed only on the page directly. Press the "Delete" button to delete the band or item with all their children items. There is no Undo function yet, so be careful.

![Page Editor image][PageEditorImage]

**Key to PageEditor features:**

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

[PageEditorImage]:images/Designer_pageEditor_withLabels.png
