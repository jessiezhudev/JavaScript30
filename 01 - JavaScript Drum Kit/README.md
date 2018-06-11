# Exercise 1: JavaScript Drum Kit
##### Target:
When you press the keyboard, the corresponding sound will play, so does the animation.

## Skills we need to grasp:
1. event system: `window.addEventListener`
2. css animation:
`transition` and `transform`
3. ES6 String Interpolation
4. `data-*` attributes

## Steps:
1. Add an eventListener for `keydown`, the function that we will provide as the callback will be defined next.
There you should know that with every keyboard letter pressed down, the parameter `event` includes a `keyCode` attribute, so that we can do the latter matching.
2. Create a function with the name that you decided on in step 1.
    
    - According to the parameter `event`, it should match with the `audio` with the `data-key`, and play it.
    - At the time, find the `div` with the right `data-key` and add `class` `playing` to it.
    - Remember to set the current playing `audio.currentTime=0` for the next `audio` to play.
3. Add an eventListener for those `key` elements to watch `transistionend`. Once it ends, remove the transition from elements.
    - This function should only be concerned with the `transform` property, as the `transition` time defines how long the transformation will take.
    