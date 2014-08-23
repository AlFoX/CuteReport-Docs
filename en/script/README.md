Script
====

In this chapter we will learn how to work with CuteReport script. Scripting feature brings an extremely high level of flexibility. Using script user can controll almost every rending step and design really complex reports. There are main script in a report that control everything from report starting till it's rendered. Some items like Memo or Barcode are supporting script in their text properties. Usualy scripting expression must be framed by [], so the scripting engine will know this is script and not regular text. But to some fields where only script is allowed expression can be written without []. Some items can reimplements [] to use something else and provide additional field to define script expression borders, like "expDelimiter" in a Memo object.


