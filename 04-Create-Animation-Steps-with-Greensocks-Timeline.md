Import TimelineMax from gsap
    - [TimelineMax Docs](https://greensock.com/docs/v2/TimelineMax)

Create a timeline, using the TimelineMax() constructor
    > const timeline = new TimelineMax()

Set a sequence of things to do
    - each sequential animation will wait until the previous animation finishes

Use pause and resume to control when your animation starts
    - if you do not pause the timeline after creation, it will run when the page loads (just like other gsap animations)
    > timeline.pause()
    - this allows you to control when the timeline will start

    Create an event and use .resume() to start your timeline (or resume from a pause if you decide to do in mid timeline)
    > timeline.resume()
    - this does not restart the timeline, just continues it wherever you paused. So once the timeline finishes, you can not redo the event (a click in the video example) to restart the animation.