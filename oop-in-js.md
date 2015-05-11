# Short guide about principles of OOP in JS

## Types
### Primitive Types
  * Boolean
  * Number
  * String
  * Null
  * Undefined

Identifying Primitives:
```javascript
typeof "text"; // "string"
typeof undefined; // "undefined"

var n = 2;
n.constructor.name; // "Number"
n.constructor === Number; // true

typeof null; // "object" - an error in JS
// to check if null use
value === null
```




### Reference Types
* Array
* Date
* Error
* Function
* Object
* RexExp


Dereferencing objects:

```javascript
var o = new Object();
o = null; // dereference - let garbage collectot free up memory
```

Identifying References:
```javascript
typeof myFun; // "function"
myFun instanceof Function; // true
listArr instanceof Array; // true
listArr instanceof Object; // true because Array was inherited from Object
Array.isArray(listArr); // true
```

## Functions

### arguments

```javascript
Array.isArray(arguments); // false

function myFn(par1) {
	arguments;
}

myFn.length; // 1 - function's arity - number of params that it's expecting
```

## Objects
### Detecting properties
```javascript
var o = {prop: false};

if (o.prop) {}; // incorrect
"prop" in o; // true, check both for own and prototype properties
o.hasOwnProperty("someMethod"); // checks only for own methods
```

### Types of Properties - accessors:
```javascript
var person = {
  _name: "Jack",

  get name() {
    console.log("Getting name");
    return this._name;
  },

  set name(value) {
    console.log("Setting name to %s", value);
    this._name = value;
  }
};

person.name
// Getting name
//"Jack"

person.name = "John"
// Setting name to John
// "John"
```

multiple properties:
```javascript
var person = {};
Object.defineProperties(person, {
	_name: {
    	value: "Jack",
        enumerable: true,
        configurable: true,
        writable: true
    },
    
    name: {
    	get: function() {},
        set: function() {},
        enumerable: true,
        configurable: true
    }
});
```

### Preventing Obj Modification

```javascript
var person = { name: "Jack "};

// preventExtensions
Object.preventExtensions(person);
Object.isExtensible(person); //false
person.lastName = "Smith";
person; // Object {name: "Jack "}

// seal
Object.seal(person); // nonextendable, nonconfigurable
delete person.name
person; // Object {name: "Jack "}
person.name = 'John'
person; // Object {name: "John"}

// freeze
Object.freeze(person); // snapshot of object, cannot be changed anything
```
## Constructors and Prototypes
http://jbt.github.io/markdown-editor/#U1ZWcM7PKy4pKk0uyS8qVkjMS1EIKMovyS+pLEgt5gIA
