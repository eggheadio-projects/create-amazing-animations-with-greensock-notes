Spin elements in 3d
    1. to rotate on the horizontal axis use the property 'rotationX'
    2. to rotate on the veritcal axis use the property 'rotationY'
    3. to rotate on the front-to-back axis use the property 'rotationZ'

Change perspective
    1. use TweenMax.set to set the 'transformPerspective' property
        > TweenMax.set(box, {transformPerspective: 200})
        - the lower the number, the more dramatic the perspective shift