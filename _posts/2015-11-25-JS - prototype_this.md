---
layout: post
title: Javascript - prototype and this
---
### this:
``` js
// 1. Property x will be added to window(global) object by executing A();
// 2. Property x will be added to new object of type A by executing new A();

> var A = function () {
    	this.x = function () {
        	//do something
    	};
};

> A();  // this === window - not what we expected, property x added to window object
< undefined

> window.x
< function () {
        //do something
    }

> A.x
< undefined

> var B = new A(); // this === new object B of type A
< undefined

> B.x
function () {
        //do something
    }
```

### prototype:
``` js
// Property y will be added to new objects Only by new X()

> var X = function () { };
X.prototype.y = function () {
    //do something Y
};
< () {
    //do something Y
}

> X
< function () { }

> X.y	// propery y is not part of object X.
< undefined

> X();	// Do nothing as empty codes in the function
< undefined

> X
< function () { }

> X.y
< undefined

> window.y
< undefined

> var Z = new X(); // Z is a object of type X. Property y added to Z.
< undefined

> Z
< X {}__proto__: X

> Z.y	// now we can access property y in object Z.
< function () {
    //do something Y
}
```
