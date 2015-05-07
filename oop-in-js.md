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
