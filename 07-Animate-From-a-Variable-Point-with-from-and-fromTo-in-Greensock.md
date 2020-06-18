Use TweenMax.from
    - [TweenMax.from docs](https://greensock.com/docs/v2/TweenMax/static.from())
    - very similar to the TweenMax.to() used before, except the properties will be where the animation starts, and its current position will be where it ends.
    ```
        document.addEventListener('click', event => {
            const { x, y } = event
            TweenMax.fromTo('#box', 1, { x, y })
        })
    ```

Use TweenMax.fromTo
    - [TweenMax.fromTo docs](https://greensock.com/docs/v2/TweenMax/static.fromTo())
    - same as the .from() except a fourth argument sets where the animation will end
    ```
        document.addEventListener('click', event => {
            const { x, y } = event
            TweenMax.fromTo('#box', 1, { x, y }, { x: 200, y: 200 })
        })
    ```