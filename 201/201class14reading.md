[<=== Back](/README.md)

# [CSS Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

Transform syntax

```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```
If a browser fully supports the `transform` property, the un-prefixed declaration (last) will overwrite the prefixed versions.

## 2D Transforms

#### Rotate
Provides the ability to rotate anelement from 0 to 360 degrees. Positive value rotates clockwise, negative counter-clockwise.

#### Scale
Allows you to change the appeared size of an element. Default scale is 1. .01 - .99 is smaller, and 1.01+ is larger.
`scaleX` and `scaleY` can be used individually to scale width and height respectively, or in a set: `scale(X,Y)`.

#### Translate
`translateX` and `translateY` will change the position of an element on the horizontal or vertical axis respectively, these can also be used as a pair: `translate(X,Y)`.

Positive values will move an element down and to the right; negative will move up and to the left.

#### Skew

Used to distort elements on the horizontal axis, vertical axis or both. Syntax is similar to `scale` and `translate`, using degrees.

### Combining Transforms

> It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. To combine transforms, list the transform values within the `transform` property one after the other without the use of commas:

```
.box-1 {
  transform: rotate(25deg) scale(.75);
}
.box-2 {
  transform: skew(10deg, 20deg) translateX(20px);
}
```

***See article for more information on Perspective, 3D Transforms, Transform Styles, and Backface Visibility.***

# [CSS Transitions and Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

## Transitions

> For a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by usein the :hover, :focus, :active, and :target pseudo-classes.

Four transition-related properties: property, duration, timing-function, and transition-delay.

Example:

```
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```

## Animations

> Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where **animations** pick up.

### Animation Keyframes

> To set multiple points at which an element should undergot a transition, use the `@keyframes` rule. The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

Example:
```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```

***See article for more on Animations***

# [8 Simple CSS3 Transitions That Will Wow Your Users](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

### 1: Fade In

```
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```

### 2: Change Color

```
.color:hover
{
        background:#53a7ea;
}
```

### 3: Grow and Shrink

```
.grow:hover  (or.shrink:hover)
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```

### 4: Rotate Elements

```
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```

### 5: Square to Circle

```
.circle:hover
{
        border-radius:50%;
}
```

### 6: 3D Shadow

```
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```

### 7: Swing

First, define a CSS animation in styles.

```
.swing:hover
{
        -webkit-animation: swing 1s ease;
        animation: swing 1s ease;
        -webkit-animation-iteration-count: 1;
        animation-iteration-count: 1;
}
```

### 8: Inset Border

```
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```

#### Additional CSS Resources

- [Pure CSS Bounce Animation](https://codepen.io/dp_lewis/pen/QWMxRR)  
- [6 Buttons Animated](https://codepen.io/retyui/pen/ByoaXV)  
- [CSS3 Animations: Keyframes](https://codepen.io/akshaychauhan/pen/dyBqVo)  
- [404](https://codepen.io/kieranfivestars/pen/MYdQxX)  

# What Google Learned About Teams

Through Project Aristotle, Google learned that the intellectual make-up, or experience level of a team does not determine its success. What seems to matter most is that all members of the group feel comfortable, welcome, and valued. We spend so much of our time working, that when we feel like we need to 'be someone else' at work, or strictly focus on the task at hand 100% of the time, we are actually hurting our progress and productivity. Emotional comfort and openness = success!
