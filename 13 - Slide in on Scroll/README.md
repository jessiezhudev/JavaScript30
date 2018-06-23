The course is all I need, since scroll is a big and important task in web development. We usually have a long list and to optimize it is always a challenge.

In this course, we're going to learn some basic knowledge associating with scroll.

## Target:
When we scroll down the page, images that enter the visible region start to appear. And when they leave the visible region, they return to their original location.

## Skills we need to grasp:
1. `debounce` function:
It is used to optimize the frequent calling of `scroll` event by limiting the time period of calling it.
2. `scroll` event:
To get the distance between the scrollbar and the top of the content, we use `scrollY`.
3. `window.innerHeight` and `offsetTop`

## Steps:
1. First we need to add an event listener for `scroll` event, pass a `checkSlide` function to `debounce` to optimize.
2. We need to know when we scroll, the distance between the top and the current visible bottom, to check if it starts to enter the imgs' regions. When half of the imgs' regions is shown, the imgs start to appear.
3. We also need to check if we have scroll down to pass the bottom of imgs, if so, imgs start to disappear.

To have a clear understanding of all the heights:

![image](https://raw.githubusercontent.com/jessiezhudev/JavaScript30/master/13%20-%20Slide%20in%20on%20Scroll/assets/slideInScroll.png)