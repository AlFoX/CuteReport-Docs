Script Signals
=================
When you write a script it means you write main function, which is processed on report generator start. In this function user can made some variable initialisation or some other preparation. You still might want more control over report processing. To make it possible olmost everyone report object has signals and you can assign your custom slot to be processed on these signals. For example you can assign your custom filter to Detail band and hide some bands while pass another. Lets review some signals and latter will see how we can use them.

**Common item Signals**:

| Signal Name | Description |
|------------|------------|
| printInit | emited when all items are preparing to be printed |
| printReset | emited when all items are cleaned up after printing |
| printBefore | emited before item printing. All property changes affects original template item |
| printDataBefore | emited when initial data for printed item is prepared. All property changes affects only current printed item and will be reset |
| printDataAfter | emited after all item's data is processed, but before actual priniting |
| printAfter | emited after item is printed on a page |

Also every item can have its own signals. You can see full signal list common with signal description in a PropertyEditor.

**Renderer Signals**:

| Signal Name | Description |
|-------------|-------------|
|reportStart()| emited after report started |
|bandBefore(CuteReport::BandInterface * band) | emited before band rendering |
|bandAfter(CuteReport::BandInterface * band) | emited after band is rendered |
|bandGemetryAfter(CuteReport::BandInterface * band) | emited when band's geometry is managed |
|itemBefore(CuteReport::BaseItemInterface * item) | emited before item rendering |
|itemAfter(CuteReport::BaseItemInterface * item) | emited after item is rendered |
|itemGeometryAfter(CuteReport::BaseItemInterface * item) | emited after item's geometry managed |
|datasetBefore(CuteReport::DatasetInterface * dataset) | emited before dataset processing |
|datasetAfter(CuteReport::DatasetInterface * dataset) | emited after dataset processed |
|datasetIteration(CuteReport::DatasetInterface * dataset) | emited on every dataset iteration |
|pageBefore(CuteReport::PageInterface * page) | emited before template page processing |
|pageAfter(CuteReport::PageInterface * page) | emited after template page [rocessing |
|formBefore(CuteReport::FormInterface * dataset) | emited before form is shown |
|formAfter(CuteReport::FormInterface * dataset) | emited after form is closed |
|reportDone() | emited after report rendering is done |

[TODO]
