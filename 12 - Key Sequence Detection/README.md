Well, this course is quite interesting. And I can apply it to my website to add more effect.

## Target:
There is a secret code defined before. You press the key on the keyboard. Once you successfully press the secret code and in the correct order, we add image to the screen.

## Steps:
1. First we define an array to store the key you pressed. And also define a `secretCode`.
2. Then we add event listener for `keyup` event. In the callback function:

    - We push each key pressed to the array we deinfed before.
    - We use `splice` function to always keep the length of the array the same as the length of the `secretCode` in order to match.
    - Turn the array into string to see if it includes the `secretCode`. If so, call `conrnify_add`. (Before that, we need add `cornify.js` first)

Then an awesome effect is done! Many unicorns are added when you press the `secretCode`.