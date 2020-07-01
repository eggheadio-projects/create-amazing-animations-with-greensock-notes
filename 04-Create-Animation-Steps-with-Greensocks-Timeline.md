# Create Animation Steps with Greensock's Timeline

📹 [Video](https://egghead.io/lessons/greensock-create-animation-steps-with-greensock-s-timeline)

1. Import TimelineMax from gsap
    - [TimelineMax Docs](https://greensock.com/docs/v2/TimelineMax)
```js
import { TimelineMax } from 'gsap'
```

2. Create a timeline, using the TimelineMax() constructor
```js
const timeline = new TimelineMax()
```

3. Set a sequence of things to do
    - each sequential animation will wait until the previous animation finishes

4. Use pause and resume to control when your animation starts
    - if you do not pause the timeline after creation, it will run when the page loads (just like other gsap animations)
    ```js
    timeline.pause()
    ```
    - this allows you to control when the timeline will start

    Create an event and use .resume() to start your timeline (or resume from a pause if you decide to do in mid timeline)
    ```js
    timeline.resume()
    ```
    - this does not restart the timeline, just continues it wherever you paused. So once the timeline finishes, you can not redo the event (a click in the video example) to restart the animation.

📹 [Previous Lesson](https://egghead.io/lessons/greensock-rotate-an-element-based-on-previous-values-with-greensock)
📹 [Next Lesson](https://egghead.io/lessons/greensock-pause-or-resume-an-animation-by-checking-isactive-with-greensock)