In this chapter, we're going to learn some console tricks! Stop using `console.log` all the time! These tricks will help your debugging efficiency!

First open up your dev tools in chrome.

1. Break on attribute modifications

Find the dom element `<p onclick="makeGreen()">×BREAK×DOWN×</p>`. Click the right mouse button. Find "Break on" and click "attribute modifications". You will see a round point in the left of the dom element. And then you click the dom element in the page. Then it will "Paused in debugger"

2. Regular

Every web developer shall know `console.log`

3. Interpolated

Dynamically update the string value loggout using `%s`

4. Styled

Change the style of the text by `%c`

5. Warning

`console.warn()`. Yeah, we must see this quite often when we use framework or debug our projects.

6. Info

`console.info()`

7. Testing

use `console.assert` to judge if the statement is true or not. If true, it returns nothing. If wrong, it returns what you specify.

8. Clearing

`console.clear()` to clear the above massive console.

9. View DOM Elements

Different from `console.log`, `console.dir` shows all the attributes of `p` element.

10. Grouping together 

When looping through an array, it is clearer to group one element together by using `console.group` to start, and `console.groupEnd` to end.

11. Counting

Simply count how many times you console by `console.count`

12. Timing

I like this method since it simply tells you how long it takes to fetch data. Begin by using `console.time`, and end by `console.timeEnd`

Don't forget `console.table` is our good friend.

All done in a nice Saturday!