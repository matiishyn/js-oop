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

http://jbt.github.io/markdown-editor/#fVPBbtswDD1PX0E4hyUFlqI7LshhQztgOyxFs92jyLStTpYMiU5jDPv3UZLttAU6X0RTj098j9IC9o3zBHWvSwR5dD1B57VVujMYwFWw292DtvB9L8RiAT+HDgMHC7j3utWkTzjmAK7gi3MGpU3xj749ok/hnpixHrPGpOCXLbHSFkshvpVoSVcDYy6s4ZM4HA6P8iSD8rojQXwKt1MQnqnYwPU1FCHxFtNWP1Hm3fm3EOIkPVjYwseNsGvlLFf2ipxfW9lihud+i5f7sN1uRyUJxWkU03mWteRad3xERQV8AGkBvefCbFkscaAaVL9B5wroA3I/psdEHlNRqYhf9PUBK/Ro1eTrFXz2Xg683kpCXu4iP69fe6tIO8vhLp3PwQOe784dM90yR+aJrub+2NJXnkZbHNti8WnkWK42ImUmbeVMhCzPIF8V6Y+yRlDOGK5wBJVHhL6DFlvnh6zm+VBnSW8NtR1YTLayGlUVIiXZx0CSSxk1Cb5MwuhA7M5zUDLrv4gsdIbAEZXkmeRKeJKBwQ16TViyMtdO7qb9tQ5pXY7Eq8tRSTYPcGoz5HlKX/ctexFem/+Sb4ZlxkoaviZiciM6ZJed9Dcr+CPezeCN+CuiUXZt0NbUpNobHtRU+D5wA5oGTtl0jeOTZh7ZBqBGEmhiCJ47VhjfKLf4Dw==
