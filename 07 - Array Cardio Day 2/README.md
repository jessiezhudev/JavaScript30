Wow, another chapter for JavaScript Array!

The three methods introduced here are not commonly used in my projects. I will try to use them after I learn this chapter.

1. `Array.prototype.some()`

This method checks if at least one element that satisfys the condition. If so, it returns true. If none of them reach the requirements, it returns false.

2. `Array.prototype.every()`

Different from the above one, it returns true only if each element in this array reaches the requirement.

3. `Array.prototype.find()`

Find is like filter, but instead returns just the one you are looking for.

4. `Array.prototype.findIndex()`

It returns the index of the element we're looking for.

## Notes
1. Difference between `slice()` and `splice()`

The `slice()` methods returns a shallow copy of a portion of an array into a new array object selected from `begin` to `end`(`end not included`)

The `splice()` method changes the contents of an array by removing existing elements and/or adding new elements.

## One more to mention
In the previous interview experiences, I've been ever asked to realize `reduce()` or some other array methods. Maybe I should try to do it later.
