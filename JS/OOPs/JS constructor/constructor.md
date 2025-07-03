### Javascript Constructor method

- Javascript constructor method is special type of method and we can create or initlize object. It is allocated memory for object.
- A class can contains only one method contructor
- Javascript allow to use parent class contrucrtor through super keyword

```js
class Parent{
    constructor(name,age){
        this.name = name;
        this.age = age;
    }
    detail(){
        return this.name + " " + this.age;
    }
}
class Child extends Parent{
    constructor(name,age,lang){
        super(name,age)
        this.lang = lang;
    }
    detail(){
        return this.name + " " + this.age + " " + this.lang;
    }
}
var v1 = new Child("kowsalya",21,"eng")
console.log(v1.detail()) //kowsalya 21 eng
```