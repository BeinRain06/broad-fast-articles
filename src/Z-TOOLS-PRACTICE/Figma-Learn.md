## FiGMA - Learn

### AUTOMATIZE YOUR WORKIN FIGMA -- NOTE

### Practicing Advices

#### 1. Create a Frame with just a text inside

- This type of frame don't require for you to firstly create a **Rectangle** container. Write the text , applied the desired dimensions (e.g - width: 200 ; height: 90). Then add `auto-layout`

- Give a specific color to he inner container of your text by choosing a color under the `fill` style property.

<br/>

#### 2. Add an underline to a Text

**First Method**

Figma does not present the css property **_text-decoration_** in their settings when inserting text in frame.

- To add an underline , someone have to create a **Rectangle**. Set the height and width of tjis one at the min-height and min-width size taken by the text.
- Move the text inside the rectangle . And under the properties of Rectangle , add a `stroke` ( similar to border in CSS ). And choose to showcase the **bottom** border under the double square icon menu.
- Go to **\*Fill** and change the opacity of the background to be null (0 ~ background transparent).

<br/>

- select the both _text_ and _rectangle_ and use the shortcut command `CTRL + G` to **group** the two elements.
- if the group has to be resizeable dynamically apply `auto-layout` (SHIFT + A).

 <br/>

**Second Mehod**

- Instead of **Rectangle** you can simply use the **Line** using the short command `L` to draw a line under the desired text.
- Adjust the length of the line to fit the length of the text , and also the Y-axis position in the panel property of Line.

<br/>

#### 3. Easily apply auto-layout

**Auto-Layout** is repsponsible to create dynamic frame in figma. It is the implementation of the CSS's layout **flexbox**.

- Create each element independently and apply the properties you want onto them (size, color. alignment, ...)
- Align all the element over the axis (X or Y) you aim to use auto layout.
- Select all the elements by left click on the mouse while pressing SHIFT
- Apply **auto-layout** (shift + A) , it will group all the elements in a resizeable frame.
- set property you want under panel auto-layout : gap , flex-direction, padding, alignment...
- Change the name of your frame to be more specific to what part of the building it represents.

<br/>

#### 4. Insert a Frame that could act independently in the Auto-layout frame Parent

- **auto-layout** is quite constraining because of the minimal set of css properties open to its use.
- To change the actual position of an element is quite disrupting . The only way to do that is by apply padding to the element , and in order to work the element need a lot of empty available inside, to not shift into a weird representation. the css property margin is missing in auto-layout, and moreover you cannot change the position (X or Y) of an element contained inside an auto-layout frame. The option is just no more available at this point, the only left option to play is **alignment**, **padding**, **gap**.

- Try to apply **grouping** when you shape a layout in a specific way that does not align all the element by the left, right or center. This will let you keep the form you want but will be difficult to resize

**N.B** : For the moment , i haven't come through a better way of dealing with this type of shape on Figma. Trying to getting more familiar with the materials i would come back to elaborate about how it is possible to achieve it , if of coures it is.
