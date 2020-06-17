To repeat timeline animation
    - use the [repeat property](https://greensock.com/docs/v2/TimelineMax/repeat())
    - a positive number will be the number of times an animation repeats, but a -1 will cause it to repeat indefinitely, use -1
    > const timeline = new TimelineMax({ repeat: -1 })

Pause and Resume by checking isActive() property
    - if an animation is currently running, its 'isActive()' property will be true
    - if paused the 'isActive()' property will be false
    - therefore a conditional is all that is needed to toggle an animation on and off

    ```
    document.getElementById("box").addEventListener('click', () => {
        if(timeline.isActive()){
            timeline.pause()
        }else{
            timeline.resume()
        } 
    })
    ```

Check it out . . . You can now pause and resume your animation by clicking on the box