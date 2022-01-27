<div align="center">
    <img src="https://github.com/Mateus20Barros/CSS-Flexbox/blob/main/assets/flexbox-css.png" width="100%" height="300px">
</div> <br>

__``This ReadMe explain about CSS Flexbox, It's very useful to build the layout pages.``__

### <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="40" height="35" align="center"/> CSS Flexbox

__The flexbox or flexible box model in CSS is a one-dimensional layout model that has flexible and efficient layouts with distributed spaces among items to control 
their alignment structure ie., it is a layout model that provides an easy and clean way to arrange items within a container. Flexbox can be useful for creating 
small-scales layouts & is responsive and mobile-friendly.__

<div align="center">
  <h2>:bricks: Container Properties</h2>
</div>

### :fire: Display 

**_This defines a flex container ``inline`` or ``block`` depending on the given value. It enables a flex context for all its direct children._**

```CSS
.container {
    display: flex;
}
```

**``NOTE: CSS columns have no effect on a flex container.``**

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








