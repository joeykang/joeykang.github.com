---
layout: post
title: Implicitly Unwrapped Optionals
---
`Implicitly Unwrapped Optionals`: 

This is a normal optional behind the scenes, but can also be used like a nonoptional value, without the need to unwrap the optional value each time it is accessed.

It is useful to remove the need to check and unwrap the optional’s value every time it is accessed, because it can be safely assumed to have a value all of the time.

It is useful when an optional’s value is confirmed to exist immediately after the optional is first defined and can definitely be assumed to exist at every point thereafter.

The primary use of implicitly unwrapped optionals in Swift is during class initialization.

### Examples:

#### 1) Optional
```swift
        var _localStr: String?
        _localStr = nil			// Can be nil as it's optional
        _localStr = "Better"
        let nCount = _localStr.characters.count    // Compile error
        let nCount2 = _localStr?.characters.count   // Possible to unwrap - optional binding
        let nCount3 = _localStr!.characters.count   // Possible to forced unwrap
```

#### 2) Implicitly Unwrapped Optional
```swift
        var _localStr: String!
        _localStr = nil			// Can be nil as it's optional
        _localStr = "Better"
        let nCount = _localStr.characters.count    // Possible without unrwapping,
                                                   // like non-optional
        let nCount2 = _localStr?.characters.count   // Possible to unwrap
        let nCount3 = _localStr!.characters.count   // Possible to forced unwrap
```

#### 3) Non optional
```swift
        var _localStr: String
        _localStr = "ABC"
        print("_localStr \(_localStr)")        
        let nCount = _localStr?.characters.count    // Compile error, Can't unwrap
```

#### 4) Non optional 
```swift
        var _localStr: String
        _localStr = nil                            // Compile error, can't be nil
```
