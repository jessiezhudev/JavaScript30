This course is a good implementation of Flex.

## Target:
Turn the whole panels vertical, and one `panel` that is clicked will expand its width and the words inside shows animation.

## Steps:
CSS part:
1. Turn the whole panels vertically by using `panels: {display: flex}`. And the inside `panel` divides evenly the extra space by `{panel: flex:1}`.
2. Turn the `p` elements in `panel` vertically and place them center by `panel: {display:flex;flex-direction:column;justify-content:center}`
3. Let the children elements of `panel` to divide the content height by three and be centered justified. 
`.panel > * {flex: 1 0 auto; display: flex;justify-content: center; align-items: center}` 
1. Hide the first element in `panel` at first by adding `.panel > *:first-child{transform: translateY(-100%)}`. At the same time, hide the last element by `.panel > &:last-child {transform: translateY(100%)}`. Also to add the state when they are pushed off. `.panel.open-active > *:first-child {transform: translateY(0)} .panel.open-active >*:last-child {transform: translateY(0)}`
2. Update the styling applied to the `panel` `open` class so that the selected panel takes up 5x the space of the other flex items:`.panel.open {
  /* ... */
  flex: 5;
}`

JS part:
1. Select all the panels and add a `click` event listener for `toggleOpen` function
2. For the `toggleOpen` function, toggle the class `open` for bigger space and `font-size`
3. When the `panel`'s transition ends, toggle the class `open-active` to show the first and last `p `element.

## One more to mention:
After taking this part of course, I find that I haven't grasped the flexbox well. Later I will take Wes Bos's flexbox class to learn more.