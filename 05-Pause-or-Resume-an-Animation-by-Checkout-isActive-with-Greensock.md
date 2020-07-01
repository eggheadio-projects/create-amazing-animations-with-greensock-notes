# Pause or Resume an Animation by Checkout isActive with Greensock

📹 [Video](https://egghead.io/lessons/greensock-pause-or-resume-an-animation-by-checking-isactive-with-greensock)

### To repeat timeline animation

- use the [repeat property](https://greensock.com/docs/v2/TimelineMax/repeat())
- a positive number will be the number of times an animation repeats, but a -1 will cause it to repeat indefinitely, use -1

```js
const timeline = new TimelineMax({ repeat: -1 })
```

### Pause and Resume by checking isActive() property

- if an animation is currently running, its 'isActive()' property will be true
- if paused the 'isActive()' property will be false
- therefore a conditional is all that is needed to toggle an animation on and off

```js
document.getElementById("box").addEventListener('click', () => {
    if(timeline.isActive()){
        timeline.pause()
    }else{
        timeline.resume()
    } 
})
```

Check it out . . . You can now pause and resume your animation by clicking on the box

📹 [Previous Lesson](https://egghead.io/lessons/greensock-create-animation-steps-with-greensock-s-timeline)
📹 [Next Lesson](https://egghead.io/lessons/greensock-manually-control-the-animation-with-progress-in-greensock)