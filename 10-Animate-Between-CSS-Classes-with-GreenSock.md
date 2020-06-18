Animate class changes
    1. create a div with a class of box
    2. establish styles for the .box class
    3. add two new classes .hover and .down and styles for each
    4. add an eventListener on the box and use [TweenMaxTo()](https://greensock.com/docs/v2/TweenMax/static.to()) to adjust the className of the box
        -make sure to add the additional classes, if you replace the class you won't be adding styles to the box, but replacing them
            > TweenMax.To(box, .25, { className: '+=hover' })
    5. Make sure to use opposite addEventListeners to remove the classNames 
        - "mouseenter" adds, "mouseout" removes
        - "mousedown" adds, "mouseup" removes