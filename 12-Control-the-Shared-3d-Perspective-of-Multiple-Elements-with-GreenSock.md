# Control the Shared 3d Perspective of Multiple Elements with GreenSock

📹 [Video](https://egghead.io/lessons/greensock-control-the-shared-3d-perspective-of-multiple-elements-with-greensock)

### Perspective
- [perspective docs](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective)
- by adjusting the perspective of the parent container you are setting the vanishing point relative to the parent container

### To Demonstrate
1. create a lot of boxes
    - use [Array.from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from), set a length to create an array
    - use [.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) to create the div elements from the array
    - .forEach then allows you to set a class of box on each div, and append it to the document.body
    - these methods can all be chained together
    - you can now add the animation, and you can add this inside the forEach

    ```js
        Array.from({length: 30})
            .map(() => document.createElement("div"))
            .forEach(box => {
                box.setAttribute("class", "box")
                document.body.appendChild(box)

                box.addEventListeners("click", () => {
                    TweenMax.to(box, 1, { rotationY: "+=180" })
                })
            })
    ```

    2. Restyle in the css 
        - on the body 
            1. remove justify-content and align-items
            2. add `flex-wrap: wrap;`
            3. add `overflow: hidden;`
        - on .box class
            - add a border so that we can see the individual boxes
        
    3. Check it out
        - as you click on different boxes you can see the perspective change based on the parent element
        - remember that a lower perspective will be more dramatic than a larger perspective

### Unstick animations
- at times animations will get 'stuck' because they weren't finished before they were activated again
To Fix
1. use the [.isTweening() method](https://greensock.com/docs/v2/TweenMax/static.isTweening()), which will return true if an animation is still running
2. use a conditional to check if the animation is still running, and only run the animation if it is not
```js
if(!TweenMax.isTweening(box)) {
    TweenMax.to(box, 1, { rotationY: "+=180" })
}
```

📹 [Previous Lesson](https://egghead.io/lessons/greensock-spin-elements-in-3d-with-greensock)
📹 [Next Lesson](https://egghead.io/lessons/greensock-loop-a-tween-forever-using-yoyo-and-repeat-with-greensock)