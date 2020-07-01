# Loop a Tween Forever Using yoyo and Repeat with GreenSock

📹 [Video](https://egghead.io/lessons/greensock-loop-a-tween-forever-using-yoyo-and-repeat-with-greensock)

### Continuously Loop Animation
1. start with a TweenMax.to()
    ```js
    TweenMax.to('element', 1, { scale: 1.25 })
    ```
2. add the repeat property
    - a positive number will repeat that many times
    - a negative one will cause it to repeat continuously, but will jump back to the start
3. use `yoyo: true;` to have the animation go back and forth (instead of restarting)
```js
TweenMax.to('element', 1, {
    scale: 1.25,
    repeat: -1,
    yoyo: true
})
```
4. GreenSock has a neat [Elastic](https://greensock.com/docs/v2/Easing/Elastic) effect
    - import it along with TweenMax from gsap
    ```js
    import { TweenMax, Elastic } from 'gsap'
    ```
    - set the ease property in your animation to any of the Elastic properties
    ```js
    TweenMax.to('element', 1, {
        scale: 1.25,
        repeat: -1,
        yoyo: true,
        ease: Elastic.easeInOut
    })
    ```

📹 [Previous Lesson](https://egghead.io/lessons/greensock-control-the-shared-3d-perspective-of-multiple-elements-with-greensock)