### Javascript objects :

- Javascript objects are mutable.
- mutable means you can change the value.

- What are the possible ways to create objects
1. Object constructor
2. Object literal
3. Object's create method
4. Function Constructor
5. Function constructor with prototype
6. ES6 classes
7. Singleton pattern

1. Object constructor

```js
const obj1 = new Object()

obj1.name = "kowsalya"
obj1.age = 21

console.log(obj1) //{ name: 'kowsalya', age: 21 }
```

2. Object literal

```js
const obj1 = {
    name : "kowsalya",
    age: 21
}

const obj2 = {}

obj2.name = "kowsalya"
obj2.age = 21

console.log(obj1) //{ name: 'kowsalya', age: 21 }
console.log(obj2) //{ name: 'kowsalya', age: 21 }
```

3. Object's create method

```js
const obj = Object.create(null)

obj.name = "kowsalya"
obj.age = 21

console.log(obj) //[Object: null prototype] { name: 'kowsalya', age: 21 }
```

4. Function Constructor

```js
function Obj(name,age){
    const obj = {}
    obj.name = name;
    obj.age = age;
    return obj;
}
let v1 = new Obj("kowsalya",21)
console.log(v1) //{ name: 'kowsalya', age: 21 }
```

5. Function consturctor with prototype

```js
function Obj(name,age){
    this.name = name;
    this.age = age;
}
Obj.prototype.lang = "eng";
let v1 = new Obj("kowsalya",21)
console.log(v1) //Obj { name: 'kowsalya', age: 21 }
```

6. ES6 classes 

```js
class Person{
    constructor(name,age){
        this.name = name;
        this.age = age;
    }
    detail(){
        return this.name + " " + this.age;
    }
}
var obj1 = new Person("kowsalya",21)
console.log(obj1) //Person { name: 'kowsalya', age: 21 }
```

7. Singleton pattern

```js
var object = new function(){
    this.name = "kowsalya";
    this.age = 21;
}
console.log(object) //{ name: 'kowsalya', age: 21 }
```

- Built In Methods in Objects

1. create
2. entries
3. keys
4. values

1. create()

```js
const people = {
    print: function(){
        return this.name + " " + this.age;
    }
}
let v1 = Object.create(people)
v1.name = "kowsalya"
v1.age = 21
console.log(v1) //{ name: 'kowsalya', age: 21 }
```

2. entries()

```js
const student = {
    name : "kowsalya",
    age : 21
}
console.log(Object.entries(student)) //[ [ 'name', 'kowsalya' ], [ 'age', 21 ] ]
```

3. keys()

```js
const student = {
    name : "kowsalya",
    age : 21
}
console.log(Object.keys(student)) //["name","age"]
```

4. values()

```js
const student = {
    name : "kowsalya",
    age : 21
}
console.log(Object.values(student)) //["kowsalya",21]
```

5. Object.is()

- Object.is() method is a useful function that allows you to see whether two values are exactly equal and without type coercion.

```js
console.log(Object.is(5,5))          //true
console.log(Object.is(0,-0))         //false
console.log(Object.is(NaN,NaN))      //true
console.log(Object.is(true,false))   //false
console.log(Object.is(null,null))    //true
console.log(Object.is("hi","hi"))    //true
console.log(Object.is("Hi","hi"))    //false
```