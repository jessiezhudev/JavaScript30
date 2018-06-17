## Target
The effect in this tutorial is quite common in some websites: when you click one box of the choices, and you press "shift" button, and click the next checkbox. The checkboxes in between will also be checked.

## Solution1
### Steps
1. Get all the checkboxes. Add event listener for each checkbox
2. Here we need to know the last checked checkbox like I said in the Target. So we define a variable named `lastChecked`
3. Like we said in Target, the checkboxes "in between" will be checked. So we define a varible "inBetween" to mark which checkboxes are in between
4. In the funciton we defined in Step 1, we need to check when we click the checkbox, whether the Shift key has been pressed down and this checkbox is checked. And when it is true, we need to loop through the checkboxes to see which checkboxes are in between. 

Well, the above solution is not that perfect enough. Since when we first load the page, we hold one Shift and click the first choice. The remaining checkboxes will all be checked. Also, it's not easy to unselect multiple checkboxes.

## Solution 2
### Steps:
1. First let's turn the checkboxes from array-like object to an array using `Array.from`. In this solution, we use `slice` to get the in-between checkboxes. And defince a variable `onOff` to mark current checked state.
2. To avoid the above `lastChecked` problem, we also judge if it exists or not.

All done! We've completed 1/3 of the course!