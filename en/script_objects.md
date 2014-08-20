Script Objects
=================

All report objects is accessible from a script by theirs name. For example if you have Memo object named memo_1 and want to set its color, you can do it by such way:
```JavaScript
memo_1.backgroundBrush = new QBrush(new QColor("#665544"));
memo_1.color = new QColor(Qt.red);
```
