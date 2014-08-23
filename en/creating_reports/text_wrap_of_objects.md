Text wrap of objects
=======
(__*commercial version only*__)

Sometimes you might want to develop report design that requires text wrapping around other objects. it can be Image or table. This is simple challenge with CuteReport. Simply add one new Memos where text should flow to. For the second Memo set property "flowTo" with the name of the first Memo where is text begin. For example if first Memo has name "memo_1", set second Memo property "flowTo" to "memo_1". Property "StretchMode" for the first Memo should be set to "DontStretch" and for the second one to "ActualHeight". That's it.

![Memo1]

Now lets render this template and see how it looks:

![Memo2]

For this example we have set **textFlag** property to **AlignJusify**. It is not necessary to set text flags to all Memos, so set them only for the first one. Every subsequent Memo inherits this setting.

Complex wrapping
-----

Making complex wrapping is not really much complicated. Take a look at the next example:

![Memo3]

As you might notice there are 3 Memo objects that used for fit text: first in the middle top contains text "[data."description"]"; second one is laying under Title memo and cover right and central part; third one is located on the bottom under all other objects. Its height set to minimal, since for some short texts it will not be used. So we do not need space wastage. Every next Memo joined to previous one by setting propery **"flowTo"** and property **stretchMode** of the last item is set to "ActualHeight". First two items do no need to stretch, so theirs property is set to "DontStretch". **"F5"** to render and voilà:

![Memo4]

You do not have to care about object insertion order, you can add Memo objects to report page in arbitrary order. Once you set correct "flowTo" name all is done. CuteReport is smart enough to understand what do you want and it hides all routine work from your sight. Enjoy!

[Memo1]:../images/memo_flow_1.png
[Memo2]:../images/memo_flow_2.png
[Memo3]:../images/memo_flow_3.png
[Memo4]:../images/memo_flow_4.png
