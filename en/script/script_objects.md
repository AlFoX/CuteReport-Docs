Script Objects
=================

All report objects is accessible from a script by theirs name. For example if you have Memo object named memo_1 and want to set its color, you can do it by such way:
```JavaScript
memo_1.backgroundBrush = new QBrush(new QColor("#665544"));
memo_1.color = new QColor(Qt.red);
```

All object prpperties thar you can see in a PropertyEditor, can be managed through the script.
Some objects support several types of property like "stretchMode" in Memo object. There are 2 types: enum and string. Use whatever you want like there:
```JavaScript
memo_1.stretchMode = "DownStretch";
memo_2.stretchMode = Memo.ActualHeight;
```
