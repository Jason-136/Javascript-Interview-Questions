### Classes in Javascript :

- Class Decalrations
- Class Expressions

1. Class Declarations:

- Classes are special type of functions
- The class is executed in strict mode

```js
class Employee{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        document.write(this.id + " " + this.name)
    }
}
var e1 = new Employee(101,"kowsi") //passing objects to a variable
var e2 = new Employee(102,"gayu")

e1.detail() //101 kowsi
e2.detail() //102 gayu
```

- class declarations is not hoisting, means you can't access before declare.

```js
var e1 = new Employee(101,"kowsi") //passing objects to a variable
var e2 = new Employee(102,"gayu")

e1.detail() 
e2.detail() 

class Employee{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        document.write(this.id + " " + this.name)
    }
}

//output : ReferenceError: Cannot access 'Employee' before initialization
```

- Re-declaring class is not allowed in class declaration

```js
class Person{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        console.log(this.id + " " + this.name)
    }
}
var e1 = new Person(101,"kowsi") //passing objects to a variable
var e2 = new Person(102,"gayu")

e1.detail() 
e2.detail() 

class Person{ //Re-declaring class 
    
}
```

2. Class Expression

- Class without name is class expression.

- Unnamed class expresion

```js
var emp = class{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        console.log(this.id + " " + this.name)
    }
}
var e1 = new emp(101,"kowsi") //passing objects to a variable
var e2 = new emp(102,"gayu")

e1.detail()  //101 kowsi
e2.detail()  //102 gayu
```

- Re-decalring class expression is allowed

```js
var emp = class{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        console.log(this.id + " " + this.name)
    }
}
var e1 = new emp(101,"kowsi") //passing objects to a variable
var e2 = new emp(102,"gayu")

e1.detail()  //101 kowsi
e2.detail()  //102 gayu

var emp = class{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        console.log(this.id + " " + this.name)
    }
}
var e1 = new emp(101,"jaya") //passing objects to a variable
var e2 = new emp(102,"kows")

e1.detail()  //101 jaya
e2.detail()  //102 kows
```

- Named class expression

```js
var emp = class Employee{ //decalrations of class
    constructor(id,name){ //initializing of object
        this.id = id;
        this.name = name;
    }
    detail(){  //declaring method
        console.log(this.id + " " + this.name)
    }
}
var e1 = new emp(101,"kowsi") //passing objects to a variable
var e2 = new emp(102,"gayu")

e1.detail() //101 kowsi
e2.detail() //102 gayu
```