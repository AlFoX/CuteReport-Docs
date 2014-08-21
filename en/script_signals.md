Script Signals
=================
When you write a script it means you write main function, which is processed on report generator start. In this function user can made some variable initialisation or some other preparation. You still might want more control over report processing. To make it possible olmost everyone report object has signals and you can assign your custom slot to be processed on these signals. For example you can assign your custom filter to Detail band and hide some bands while pass another. Lets review some signals and latter will see how we can use them.

Item Signals

| Signal Name | Description |
|------------|------------|
| printInit | emited when all items are preparing to be printed |
| printReset | emited when all items are cleaned up after printing |
| printBefore | emited before item printing. All property changes affects original template item |
| printDataBefore | emited when initial data for printed item is prepared. All property changes affects only current printed item and will be reset |
| printDataAfter | emited after all item's data is processed, but before actual priniting |
| printAfter | emited after item is printed on a page |


