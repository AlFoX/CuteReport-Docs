Using global report variables in a script
====================

Any global variable that is defined in a report could be accessed from a script. The variable name should be writen in such kind: ${my\_variable} without spaces not between rounding signs not in variable name. It is 2 recommended way if you want to give your variable some complex name like "my super duper variable". First way is to replace spaces with "\_" sign. and second one is to remove spaces and use capital letter on the every word after first one, oor even including first one like: mySuperDuperVariable or MySuperDuperVariable. Also it's important to not use name that other objects already have, because report variable are also objects like any other report objects. Internally script engine use special named object to represent global variables and rendered's variables like "\_page", "\_pages" and predict variable names with "\_". So using "\_" in begin of your varibale name is highly not recommended. On other hand you can have local script variable and global report variable with the same name:
```JavaScript
var myVar = 5;
print(${myVar});
print(myVar);
```
Withing script variables "myVar" and "${myVar}" are totally diferent objects. Once you mentioned you global variable in the script it will be automatically added to the report variable list if it's not still exists there. Lets try it.
Open new empty report, go to the "Script" tab and enter {$test}. Now switch to the "Reports" tab. You will see your variable in the list of variables and could test your script by setting any test value for te variable.

![GlobalVariablesList]


[GlobalVariablesList]:../images/script_2.png
