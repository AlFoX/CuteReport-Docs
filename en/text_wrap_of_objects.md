Text wrap of objects (commercial version only)
-----------
Sometimes you might want to develop report design that requires text wrapping around other objects. it can be Image or table. This is simple challenge with CuteReport. Simply add one new Memos where text should flow to. For the second Memo set property "flowTo" with the name of the first Memo where is text begin. For example if first Memo has name "memo_1", set second Memo property "flowTo" to "memo_1". Property "StretchMode" for the first Memo should be set to "DontStretch" and for the second one to "ActualHeight". That's it.

![Memo1]



![Memo2]

[Memo1]:../images/memo_flow_1.png
[Memo2]:../images/memo_flow_2.png
