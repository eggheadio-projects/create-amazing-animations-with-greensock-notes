# Animate Between CSS Classes with GreenSock

📹 [Video](https://egghead.io/lessons/greensock-animate-between-css-classes-with-greensock)

### Animate class changes
1. create a div with a class of box
2. establish styles for the .box class
3. add two new classes .hover and .down and styles for each
4. add an eventListener on the box and use [TweenMax.to()](https://greensock.com/docs/v2/TweenMax/static.to()) to adjust the className of the box
    - make sure to add the additional classes, if you replace the class you won't be adding styles to the box, but replacing them
    ```js
    TweenMax.to(box, .25, { className: '+=hover' })
    ```
5. Make sure to use opposite addEventListeners to remove the classNames 
    - "mouseenter" adds, "mouseout" removes
    - "mousedown" adds, "mouseup" removes

📹 [Previous Lesson](https://egghead.io/lessons/greensock-stop-animations-with-killtweensof-and-killall-in-greensock)
📹 [Next Lesson](https://egghead.io/lessons/greensock-spin-elements-in-3d-with-greensock)