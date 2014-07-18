Memo object
----
The Memo object has many great features to draw text on a page. It can draw text in a frame and can be filled with some color. The text can be displayed using any font with any size and style. All the properties can be set using Property Editor ![TODO: or visually with the help of the toolbar]:

[ToolBarImage]

Here you can see some samples:

![memoSamples]


Let's look close at the Memo item features. 

**Text Aligning**

We will make a simple example of Memo with two lines of text:

*First text line with some very useful info.*<br>
*Second line with some other useful info.*

Enable Memo frame from Property Editor and resize item up to 90x30 mm using mouse or Property Editor. As you can see now Memo can display not only a single line but several lines os text as well. Try to reduce Memo width to 50 mm. Obviously, lines can not fit to the object's border and will be wrapped. This is controlled by TextFlags::TextWordWrap object property. If it is disabled any long line will be cut short. Lets play with other TextFlags and see what we can have.

![memoSamples1]

**Rotating**

Lets take a look at the other feature: rotation. Any object including Memo can be rotated to any angle in degree range 0..360. Set required angle in the PropertyEditor by changing property "rotation". Memo borders will be aligned accordingly, so you don't need to care about the borders.

![memoSamples3]


**HTML tags**

Memo object allow most of HLML tags. Tags can be placed within Memo text. Tags are disabled by default. For HTML tags detection set property "allowHTML" to "true". There are some examples below.

\<i\>Memo\</i\> \<b\>example\</b\><br>
E = mc<sup>2</sup><br>
A\<sub\>1\</sub\> = B\<sup\>2\</sup\><br>
this is a usual text, \<font color=red\>and this is a red one\</font\><br>
this is a usual text, \<font color="#FF8030"\>and this is an orange one\</font\>

![memoSamples4]

Other Memo properties: [TODO]
- stretchMode: object stretchability to fit text
- showStretchability: do stretching not only on rendered page, but on Designer' PageEditor too
- allowHTML: enterpret all HTML tags
- allowExpressions: detect scripting expressions and calculate them
- expressionDelimiter: two string separated by comma which means begin and end of scripting block.
- stretchFont: set automatic font size to fit Memo text within Memo width

[memoSamples]:../images/memo_samples.png
[memoSamples1]:../images/memo_samples1.png
[memoSamples3]:../images/memo_samples3.png
[memoSamples4]:../images/memo_samples4.png
