Create a box in index.html
    1. div with id="box"

Use gsap to style box
    1. use TweenMax.set() - syntax below
        > TweenMax.set("selectedElement", {properties})
        take a look at [Common CSS Properties Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference) to see how CSS properties are defined in javascript

To rotate the box
    1. use TweenMax.to() inside the eventListener callback function
    ```
    document.addEventListener('click', event => {
        TweenMax.to("#box", 0.5, {
            rotation: 30
        })
    })
    ```
    - expected behavior will be that a 'click' anywhere on the document will set off an animation on the div with id="box" ("#box") to change it's 'rotation' to 30 degrees
    - additional clicks will appear to have no effect since the rotation is already at 30 degrees
    2. to rotate on additional clicks change 
        > rotation: 30
        
        to 

        > rotation: "+=30"

        - this will add 30 degrees to the current rotation value and animate the change to that new rotation value
        - now additional clicks will continue to rotate the #box