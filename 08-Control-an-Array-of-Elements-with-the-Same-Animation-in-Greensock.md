Create 100 boxes and place them randomly
    1. use [Array.from() method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from) to create an array with 100 div elements
    2. loop through the array with a [.forEach() method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) and set the properties with [TweenMax.set()](https://greensock.com/docs/v2/TweenMax/static.set()).
    3. Mount each div in the .forEach() with 
        > document.body.appendChild(div)

    All together
    ```
        const divs = Array.from({length: 100}, () => 
            document.createElement('div')
        )

        divs.forEach(div => {
            TweenMax.set(div, {
                position: "absolute",
                x: `${Math.random() * window.innerWidth}px`,
                y: `${Math.random() * window.innerHeight}px`,
                width: 20,
                height: 20,
                backgroundColor: 'green',
                border: "3px solid black"
            })
            
            document.body.appendChild(div)
        })
    ```

    -check it out . . . if you refresh the page the boxes will be randomly placed again due to the [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) used to set the x and y properties

Collect the divs together with a click
    1. add and event listener for a click event, you will need the event param
        > document.addEventListener("click", event => {})
    2. use the x and y properties from the click
        > const { x, y } = event
    3. use [TweenMax.to()](https://greensock.com/docs/v2/TweenMax/static.to()) to animate them to the location of your click
        > TweenMax.to(divs, 1, { x, y })
        - notice the selected Element is the entire array (divs)

    All together
    ```
       document.addEventListener("click", event => {
            const { x, y } = event

            TweenMax.to(divs, 1, { x, y })
        })
    ```