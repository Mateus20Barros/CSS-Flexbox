<div align="center">
    <img src="https://github.com/Mateus20Barros/CSS-Flexbox/blob/main/assets/flexbox-css.png" width="100%" height="300px">
</div> <br>

__``This ReadMe explain about CSS Flexbox, It's very useful to build the layout pages.``__

### <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="40" height="35" align="center"/> CSS Flexbox

**The flexbox or flexible box model in CSS is a one-dimensional layout model that has flexible and efficient layouts with distributed spaces among items to control 
their alignment structure. It's a layout model that provides an easy and clean way to arrange items within a container. Flexbox can be useful for creating 
small-scales layouts is responsive and mobile-friendly.**

<div align="center">
  <h2>:package: Container Properties</h2>
</div>

### :fire: Display 

**_This defines a flex container ``inline`` or ``block`` depending on the given value. It enables a flex context for all its direct children._**

```CSS
.container {
    display: flex;
}
```

***NOTE: CSS columns have no effect on a flex container.***

---

### :fire: Flex Direction

**_This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is aside from optional wrapping a 
single-direction layout concept. Think of flex items as primarily laying out either in horizontal ``row`` or ``vertical`` columns._**

```CSS
.container {
    flex-direction: ... ;
}
```

- **``row`` - left to right | right to left - *by default***
- **``row-reverse`` - right to left | left to right.**
- **``column`` - same as row but top to bottom.**
- **``column-reverse`` - same as row-reverse but bottom to top.**

---

### :fire: Flex wrap

**_By default,  flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property._**

```CSS
.container {
    flex-wrap: ... ;
}
```

- **``nowrap`` - all flex items will be on one line - *( by default )***
- **``wrap`` - flex items will wrap onto multiple lines,  from top to bottom.**
- **``wrap-reverse`` - flex items will wrap onto multiple lines from bottom to top.**

---

### :fire: Flex flow

**_This is a shorthand for the ``flex-direction`` and ``flex-wrap`` properties, which together define the flex container's main and cross axes._**

**``The default value is row nowwrap``**

```CSS
.container {
    flex-flow: ... ;
}
```

---

### :fire: Justify content

**_This defines the alignment along the main axis. It helps distribute extra free space left over when either all the flex items on a line are inflexible, 
or are flexible but have reached their maximum size. It also exerts some control over the alignment of items when they overflow the line._**

```CSS
.container {
    justify-content: ... ;
}
```

- **``flex-start`` - items are packed toward the start of the flex-direction - *( by default )***
- **``flex-end`` - items are packed toward the end of the flex-direction.**
- **``center`` - items are centered along the line.**
- **``space-between`` - items are evenly distributed in the line, first item is on the start line, last item on the end line.**
- **``space-around`` - items are evenly distributed in the line with equal space around them.**
- **``space-evenly`` - items are distributed so that the spacing between any two items and the space to the edges is equal.**

---

### :fire: Align items

**_This defines the default behavior for how flex items are laid out along the cross-axis on the current line. Think of it as the justify-content version for 
the cross-axis perpendicular to the main-axis._**

```CSS
.container {
    align-items: ... ;
}
```

- **``stretch`` - stretch to fill the container still respect "min-width" and "max-width".**
- **``flex-start`` - items are placed at the start of the cross-axis.**
- **``flex-end`` - items are placed at the end of the cross-axis.**
- **``center`` - items are centered in the cross-axis.**
- **``baseline`` - items are aligned such as their baselines align.**

---

### :fire: Align content

**_This aligns a flex container's lines within when there is extra space in the cross-axis, similar to how ``justify-content`` aligns within the main-axis._**

```CSS
.container {
    align-content: ... ;
}
```

- **``flex-start`` - items packed to the start of the container.**
- **``flex-end`` - items packed to the end of the container.**
- **``center`` - items centered in the container.**
- **``space-between`` - items evenly distributed,the first line is at the start of the container while the last one is at the end.**
- **``space-around`` - items evenly distributed wuth equal space around each line.**
- **``space-evenly`` - items are evenly distributed wuth equal space around them.**
- **``stretch`` - lines stretch to take up the remainig space.**

---

### :fire: Gap, Row gap & Column gap

**_The gap property explicitly controls the space between flex items. It applies that spacing only between items not on the outer edges._**

```CSS
.container {
    display: flex;
    
    gap: 10px;
    row-gap: 10px;
    colunm-gap: 10px;
}
```

**_The behavior could be thought of as a minimum gutter,as if the gutter is bigger some how because of something like <br> ``justify-content: space-between;`` 
then the gap will only take effect if that space would end up smaller. It is not exclusively for flexbox , gap works in grid and multi-colum layout as well._**

<br>

<div align="center">
  <h2>:jigsaw: Items Properties</h2>
</div>

### :sparkles: Order

**_By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container._**

```CSS
.item {
    order: 5;
}
```

**_Items with the same order revert to source order._**

---

### :sparkles:Flex grow

**_This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion. I dictates what amount of the 
avaliable space inside the flex container the item should take up._** <br>

**_If all items have ``flex-grow`` set to 1, the remaining space in the container will be distribuited equally to all children. If one of the children has 
a value of 2, that child would take up twice as much of the space either one of the others or it'll try, at least._**

```CSS
.ietms {
    flex-grow: 4;
}
```

**_Negative numbers are invalid._**

---

### :sparkles: Flex shrink

**_This is define the ability for a flex item to shrink if necessary._**

```CSS
.item {
    flex-shrink: 3;
}
```

**_Negative numbers are invalid._**

---

### :sparkles: Flex basis

**_This define the default size of an element before the remaining space is distribuited. It can be a length ``( "20%", "5rem", etc... )`` or a keyword. 
The auto keyword means "look at my width or height property" which was temporarily done by the main-size keyword until deprecated. The content keyword 
means size it based on the on the item's content, this keyword isn't well supported yet, so it's hard to test and harder to know what its brethren 
max-content, min-content and fit-content do._**

```CSS
.items {
    flex-basis: auto;
}
```

- **_If set to ``0`` the extra space around content isn't factored in._** <br> 
- **_If set to ``auto`` the extra space is distributed based on its flex-grow value._**

---

### :sparkles: Flex

**_This is the shorthand for ``flex-grow``, ``flex-shrink`` and ``flex-basis`` combined. The second and third parameters are optional. The default 
is ``0 1 auto`` but if you set it with a single number value, like ``flex: 5;`` that changes the ``flex-basis`` to ``0%``_ so it's like setting 
``flex-grow: 5;``, ``flex-shrink: 1;`` and ``flex-basis: 0%``.**

```CSS
.item {
    flex: none / flex-grow / flex-shrink / flex-basis ;
}
```

**_It's recommended that you use this shorthand property rather than set the individual properties. <br>
The shorthand sets the other values intelligently._**

---

### :sparkles: Flex self

**_This is allows the default alignment or the one specified by align-items to be overridden for individual flex items. Please see the ``align-items`` 
explanation to understand the available values._**

```CSS
.items {
    align-self: auto / flex-start / flex-end / center / baseline / stretch ;
}
```

**_Note that ``float``, ``clear`` and ``vertical-align`` have no effect on a flexitem._**

<br>

:book: **For more informations about that one, you can see [CSS tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)**

<div align="right">
    :octocat: Made by Mateus Barros :rocket:
</div>

---
