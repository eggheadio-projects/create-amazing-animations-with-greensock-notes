Manually Control animation
    - will use a wheel event listener and the [progress property](https://greensock.com/docs/v2/TimelineMax/progress()) on the timeline
    ```
    document.addEventListener('wheel', () => {
        timeline.progress(timeline.progress() + 0.1)
    })
    ```
    - this only advances the animation ( + 0.1 )

    Animate forward and backwards with wheel event
        - use the event object and the .wheelDelta property to determine if you are scrolling up or down
        - a conditional then allows you to either add to the progress or subtract from it 
        ```
        if(event.wheelDelta > 0){
            timeline.progress(timeline.progress() + 0.1)
        } else {
            timeline.progress(timeline.progress() - 0.1)
        }
        ```
        - check it out . . . Pretty cool, but a little choppy right?
    
    Animate smoothly with TweenMax.to
        - .progress is a property, we know we can animate to a property value with a TweenMax.to
        > TweenMax.to("selectedElement", duration {properties})
        - combine the above timeline.progess with TweenMax.to
        ```
        document.addEventListener('wheel', event => {
            if(event.wheelDelta > 0){
                TweenMax.to(timeline, .25, {progress: "+=0.1"})
            } else {
                TweenMax.to(timeline, .25, {progress: "-=0.1"})
            }
            
        })
        ```
        - notice that the "selectedElement" is timeline, not "#box". That is because the progress is a property on the timeline, not on the box div.