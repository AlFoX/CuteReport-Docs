Multi-lined text display
------

Let's proceed further and learn how to manage multi-line text. In the prevvious chapter we have learned how to make new report, create dataset and connect dataset to a band. So lets do it:
* create new empty report
* add new SQL dataset and use test sqlite dataset "animals.db" which you can find along the CuteReport destribution or take it there: https://github.com/AlFoX/CuteReport_examples/tree/master/datasets. 
* add Detail band
* put 2 Memos on the band: first is the animal name, second one is the animal description
* put Image item to the right side of the band

[TemplateReady]

Now lets look closer how to make Dataset. After you have added SQLdataset, point it to your "animals.db" file, set Driver - "SQLITE" and add sql query - "select * from animal". Press "Test it" and check if all fine. Below you can see how it should look.

[Dataset]

When this part is completed, go back to the PageEditor and set correct fields to display for the Memo's. First topmost Memo is the animal's name. So double-click it and type: [data."name"]. Users of the commercial version, can simply click on the appeared button on the rightside of the Memo and choose field from the dropdown list. If it doesn't appear check if your band is connected to correct dataset, ie dataset under Memo has filled field "dataset". Set Bold text for the animal name, by clicking on the "font" property in the PropertyEditor. Now go to the second Memo. It's description. So type or select there: [data."description"]. Simple, huh? Lets look the result and render our report (press "F5"):

[WrongExample]

Doesn't look good, right? Some of the descriptions were cut-off. Sure we can simply change description Memo height to fit largest text, but there are some disadvantages: 
* paper wasting, since we will not use entire Memo's room for small text
* you newer know how long text will be ot it can be changed in future
* it just doesn't look pretty :)

Go ahead and fix it: set Memo property "stretchMode" to "ActualHeight" and generate report.

[CorrectExample]


[TemplateReady]:../images/multiline_text1.png
[Dataset]:../images/multiline_text2.png
[WrongExample]:../images/multiline_text3.png
[CorrectExample]:../images/multiline_text4.png
