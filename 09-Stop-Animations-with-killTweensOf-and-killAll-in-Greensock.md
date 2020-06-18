Stop animations by clicking on target
    1. Use the randowm boxes from previous video but place the animation outside of the eventListener and set them to animate to a fixed point
    2. inside the click even function use [TweenMax.killTweensof()](https://greensock.com/docs/v2/TweenMax/static.killTweensOf()) and use event.target to select the box clicked on
        > TweenMax.killTweensOf(event.target)

Stop all animations
    1. use [TweenMax.killAll()](https://greensock.com/docs/v2/TweenMax/static.killAll()) instead to stop all animations
    2. optionally you can pass an argument of true in to cause all animations to complete
        > TweenMax.killAll(true)