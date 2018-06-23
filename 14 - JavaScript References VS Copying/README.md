In this chapter, we're learning about JavaScript variable referencing vs. copying. First We need to have a clear understanding of primitive types and object types and how they are manipulated. 

## Primitive types
**Primitive types** are _maniputlated by value_. The following types are considered **primitive types** in JavaScript.
- Number
- String
- Boolean
- null
- Undefined

This means when you define a variable as a primitive type, and then you define another variable that equals to the previously defined variable. The second variable will copy the value of the first. Any changes to either one of the variable will not affect another.

Example:

```JavaScript
let age = 100
let age2 = age
console.log(age===age2) //true
age2 = 200
console.log(age===age2,age,age2) // false, 100, 200

```

## Object types
**Object types** are _manipulated by reference_. If we're being really technical, almost everything can be an object in JavaScript, but let's try not to get hung up on technicalities.

**Object types** in JavaScript:
- Object 
- Function
- Array
- Set

Let's define a variable as an object, and define a second variable equal to the first one.

```JavaScript
const me = {name: 'Jessie', age: 26}
const me2 = me
console.log(me === me2) // true
```

If we update the property of either variable, each one will reflect the change.

```JavaScript
me2.age = 25
console.log(me === me2) //true
console.log(me) //{name: "Jessie", age: 25}
```

This is beacause `me2` does not copy the value of `me`, it only copys the reference to the object defined in `me`. Any changes applied to the object will have influence on all variables referencing to that original object. So if we need to copy a variable, we need to create a new object to copy all the attributes.

```JavaScript
const me3 = Object.assign({}, me)
console.log(me3) // {name: 'Jessie', age: '25'}
console.log(me3 === me) // false. It's a new object instance. 
me3.name = 'Joe'
console.log(me) // {name: 'Jessie', age: '25'} not changed
```
**However, it is only shallow copy which means if we copy objects containing object, we only copy the first level. Anything deeper than that will still be a reference. Then we need deep clone. You can find the method in Loadash**

Other ways of copying objects will be presented in the code.