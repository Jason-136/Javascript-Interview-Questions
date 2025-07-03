### Javascript prototype 

```js
function Obj(name,age){
    this.name = name;
    this.age = age;
}
Obj.prototype.fullName = function(){
    return this.name + " " + this.age;
}
var v1 = new Obj("kowsalya",21)
var v2 = new Obj("kowsi", 22)
console.log(v1.fullName()) //kowsalya 21
console.log(v2.fullName()) //kowsi 22
```

```js
function Obj(name,age){
    this.name = name;
    this.age = age;
}
Obj.prototype.lang = "eng"
var v1 = new Obj("kowsalya",21)
var v2 = new Obj("kowsi",22)
console.log(v1.lang) //eng
console.log(v2.lang) //eng
```