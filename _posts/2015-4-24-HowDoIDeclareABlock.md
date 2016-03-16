---
layout: post
title: How Do I Declare A Block in Objective-C
---

### As a local variable:
```objective-c
returnType (^blockName)(parameterTypes) = ^returnType(parameters) {...};
```

### As a property:
```objective-c
@property (nonatomic, copy) returnType (^blockName)(parameterTypes);
```

### As a method parameter:
```objective-c
- (void)someMethodThatTakesABlock:(returnType (^)(parameterTypes))blockName;
```

### As an argument to a method call:
```objective-c
[someObject someMethodThatTakesABlock:^returnType (parameters) {...}];
```
### As a typedef:
```objective-c
typedef returnType (^TypeName)(parameterTypes);
TypeName blockName = ^returnType(parameters) {...};
```
### Reference
<http://fuckingblocksyntax.com> 