Using global report variables in a script
====================

Any global variable that is defined in a report could be accessed from a script. The variable name should be writen in such kind: ${my\_variable} without spaces not between rounding signs not in variable name. It is 2 recommended way if you want to give your variable some complex name like "my super duper variable". First way is to replace spaces with "\_" sign. and second one is to remove spaces and use capital letter on the every word after first one, oor even including first one like: mySuperDuperVariable or MySuperDuperVariable. Also it's important to not use name that other objects already have, because report variable are also objects like any other report objects. Internally script engine use special named object to represent global variables and predict variable name with "\_\_". So using "\_\_" in begin of your varibale name is not recommended. But you can have local script variable and global report variable with the same name:
```JavaScript
var myVar = 5;
print(${myVar});
print(myVar);
```
Withing script variables "myVar" and "${myVar}" are totally diferent objects.
