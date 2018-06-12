# Exercise 3: CSS Variables

This chapter is quite fresh to me since it uses CSS variables.

The difference between SASS and CSS variables is that SASS cannot be changed when it finishes being compiled. But CSS variables can be changed by JS.

## Target:
While changing the range of `spacing blur base color`, change the corresponding style of the img at the same time.

## Skills we need to grasp:
1. How to write CSS variables
2. How to set element's style property:
`document.documentElement.setProperty`
3. How to get all the `data-*` property:
`dataset`

## Steps:
1. Set the base CSS variables and set the img property according to the variables.
2. Add event listener to those `input`, to handle update.listening for change and mouse movements on the inputs.
3. To handle with `handleUpdate` function defined in Step 2. Get the name, value, and data-sizing of the changing input, and reset the CSS variables.

