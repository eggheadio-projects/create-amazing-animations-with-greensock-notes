Continuously Loop Animation
    1. start with a TweenMax.to()
        > TweenMax.to('element', 1, { scale: 1.25 })
    2. add the repeat property
        - a positive number will repeat that many times
        - a negative one will cause it to repeat continuously, but will jump back to the start
    3. use yoyo: true; to have the animation go back and forth (instead of restarting)
    ```
    TweenMax.to('element', 1, {
        scale: 1.25,
        repeat: -1,
        yoyo: true
    })
    ```
    4. GreenSock has a neat [Elastic](https://greensock.com/docs/v2/Easing/Elastic) effect
         - import it along with TweenMax from gsap
         > import { TweenMax, Elastic } from 'gsap'
         - set the ease property in your animation to any of the Elastic properties
         ```
        TweenMax.to('element', 1, {
            scale: 1.25,
            repeat: -1,
            yoyo: true,
            ease: Elastic.easeInOut
        })
        ```