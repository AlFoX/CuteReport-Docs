Bands
====

Bands are designed for positioning items on a page. Each band has its own position and functionality. CuteReport has some special bands designer to represent data from a dataset. Dataset contains structured data organized into rows(lines) which have one or more columns(fields). To print data from datasets CuteReport uses these special bands named "Detail...". To make it work, add one or more such bands to the page, connect them to the dataset and place Memo items on them. Once band is connected to the dataset, Memo will have button on the right side with the dropdown list of dataset's fields names (commercial version only).
While rendering process these bands will be printed on the rendered page. "Detail" band will be printed once per dataset row, DetailHeader and DetailFooter will be printed accordingly to theirs "condition" property. If there is no free space to print new band, new rendered page will be created before continue. New page will print all page headers and footers before continue to print Detail bands.


There are some bands included into standard package and theirs short description:

* __PageHeader__: displays all nested items on the top of the page
* __PageFooter__: displays all nested items on the bottom of the page
* __Title__: displays all nested items on the report begin
* __Summary__: displays all nested items on the report end
* __Detail__: must be joined to a dataset and displays all nested items on every dataset iteration
* __DetailHeader__: must be joined to a dataset and can be shown on every dataset iteration or when "condition" property calculated as "true". It can be used for grouping for show group header
* __DetailFooter__: must be joined to a dataset and can be shown on every dataset iteration or when "condition" property calculated as "true". It can be used for grouping for show group summary
* __Overlay__: can be located anywhere on a page without respecting any layouts. Can be used as carrier band for foregraund, background, watermarks.
