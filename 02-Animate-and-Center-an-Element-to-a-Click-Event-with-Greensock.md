# Animate and Center an Element to a Click Event with Greensock

📹 [Video](https://egghead.io/lessons/greensock-animate-and-center-an-element-to-a-click-event-with-greensock)

Create a box with basic styles in index.html

1. div with id="box"
2. Create css file and link it in the head of your html
3. basic styles
```css
#box {
    width: 25px;
    height: 25px;
    background-color: deepskyblue
}
```

Now start your server
```
yarn dev
```

Switch to your index.js file to add event

1. Add event listener
```js
document.addEventListener("click", event => {}) 
```

2. add TweenMax inside event listener
```js
document.addEventListener("click", event => {
    TweenMax.to("#box", 1, { x: 100, y: 100})
})
```
TweenMax syntax is
```
TweenMax.to("selectedElement", duration(in seconds), {properties})
```

TweenMax will move the "selectedElement" to the {properties} in the time set by duration.

So the code from 2. will move our div with id box to x = 100px and y = 100px in 1 second.

If you want to move the box to the location of your click a few additional steps are necessary.
1. grab the location of your click
    - this can be done by accessing the clientX and clientY properties from the click event
    ```js
    document.addEventListener("click", event => {
        const {clientX, clientY} = event
    })
    ```
2. Use the locations inside your TweenMax
    ```js
    document.addEventListener("click", event => {
        const {clientX, clientY} = event

        TweenMax.to("#box", 1, { x: clientX, y: clientY})
    })
    ```
    - check it out . . . not quite right just yet is it? 
3. eliminate body margin
    - inside your CSS file
    ```css
    body {
        margin: 0;
    }
    ```
    - check it out . . . now the corner lines up with the pointer click, but to make it center on the pointer keep going.
4. Align the center of the box to the x and y coordinates
    - use TweenMax.set, syntax looks like this
        `TweenMax.set("selectedElement", {properties})`
        - this will set the {properties} of the "selectedElement" from the get go and keep them throughout animation
    ```
    TweenMax.to("#box", {xPercent: -50, yPercent: -50})
    ```
    - check it out . . . nice Right!?

📹 [Previous Lesson](https://egghead.io/lessons/greensock-setup-greensock-as-a-module-with-parcel) 📹 [Next Lesson](https://egghead.io/lessons/greensock-rotate-an-element-based-on-previous-values-with-greensock)