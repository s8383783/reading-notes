## Readings: CSS Tips and Tricks
***
### [CSS Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)
- > With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.
- The `transform` property come ins two different settings:
  * two-dimensional
    * > Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes.
  * three-dimensional
    * > Three-dimensional transforms work on both the x and y axes, as well as the z axis.
- 2D Rotate: The `transform` property can handle multiple types of values.
  * The `rotate` value provides the ability to rotate an element from 0 to 360 degrees; positive values with rotate clockwise and negative values will rotate counterclockwise.
- 2D Scale: The `scale` value within the `transform` property allows you to change the appeared size of an element.
  * The scaleX value will scale the width of an element while the scaleY value will scale the height of an element.
- 2D Translate: The `translate` value works a bit like that of relative positioning by utilizing `translateX` and `translateY`
- There are many more values that are used with 2D & 3D Transformations such as:
  * `Skew`, `Cube`. `transform-origin`, `perspective`

### [Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)
- > Transitions: for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target pseudo-classes`.
- Four transitions related properties: (The first three are the most popular)
  * `transition-property`
    * Determines exactly what properties will be altered in conjunction with the other transitional properties.
  * `transition-duration`
    * The duration in which a transition takes place is set
  * `transition-timing-function`
    * Used to set the speed in which a transition will move
  * `transition-delay`
    * Used to set a delay
- Animations: A great skill to have because it builds out visual interactions from one state to another
  * The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated.
  * Animation Name: To do so, the animation-name property is used with the animation name, identified from the @keyframes rule, as the property value.
  * 
### [8 simple CSS3 transitions that will wow your users](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)
1. Fade in: Fade in effects are coded in two steps: first, you set the initial state; next, you set the change
2. Change color: Changing colors used to involve a ton of math but now we can simply use the `background` property.
3. Grow & Shrink: We can use the `transform` property to accomplish grow and shrink
4. Rotate elements: covered above
5. Square to circle: you can accomplish this with the `BORDER-RADIUS` property
6. 3D shadow: This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.
7. Swing: Using @keyframes which is covered above
8. Inset border: We can use the transition in a border using an inset box shadow.
### [6 Buttons animated](https://codepen.io/retyui/pen/ByoaXV)
- Check out these cool button animations!
### [CSS3 Animations: Keyframes](https://codepen.io/akshaychauhan/pen/oAfae)
- Great example of some more animations
### [404](https://codepen.io/kieranfivestars/pen/MYdQxX)
- Great example of some more animations
### [Pure CSS Bounce Animation](https://codepen.io/dp_lewis/pen/gCfBv)
- Fun animation!
***