Oops, long time no update my JavaScript 30, since the work load was quite heavy.

Today we're gonna learn about _event capture_, _propagation_, _bubbling_ and _once_.

#### Bubbling
Well, it's quite easy to understand _bubbling_. It's when you click the child elements, actually you're also click one part of the parent elements. So the events bound to the parent elements will also be triggered. The way to stop it is to use `stopPropagation()` in click events.

Like the example in this chapter:
```
 const divs = document.querySelectorAll('div')
 function logText() {
   console.log(this.classList.value)
 }
 divs.forEach((div)=>{
   div.addEventListener('click', logText)
 })
```
When you click the inner `div` whose `className` is three, the parent `divs` are also clicked. So the control panel consoles "three", "two", "one".

When you add `stopPropagation()` in the `logText`, it successfully stop the bubbling and only consoles `three`.

```
 function logText(e) {
   e.stopPropagation()
   console.log(this.classList.value)

 }
```

#### Capture

For _capture_, it means when you click the child elements, the browser captures the event from up to bottom. The default value of `capture` is false. When you set the `capture` to be true. It consoles the parent element's `className` 'one'.

```
 divs.forEach((div)=>{
   div.addEventListener('click', logText, {
     capture: true
   })
 })
```

#### Once
If you want an event to fire only once, you can add a `once` attribute.

```
 divs.forEach((div)=>{
   div.addEventListener('click', logText, {
     capture: false,
     once: true
   })
 })
```

Well, it feels so good to finish a chapter! Keep firing!