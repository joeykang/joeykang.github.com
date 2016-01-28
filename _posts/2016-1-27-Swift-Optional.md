---
layout: post
title: Optional/Non-optional in Swift
---
`Optional variable`: its content can exist or be empty(nil)

`Non-optional variable`: its contect must exist

### Examples:

#### 1) Non optional
```
        var _localStr: String
        print("unwrapped-1 \(_localStr)")  ==> Compile error: not initialized
```
#### 2) Non optional
        var _localStr: String
        _localStr = "ABC"
        print("_localStr \(_localStr)")    ==> Compile OK, No need to unwrap
        ==> Output: _localStr ABC
#### 3) Non optional 
        var _localStr: String
        _localStr = "ABC"
        let _strLen = _localStr!.characters.count  ==> Compile error: forced unwrapping non-optional value
#### 4) Non optional
        var _localStr: String
        _localStr = "ABC"
        let _strLen = _localStr?.characters.count  ==> Compile error: forced optional chaining non-optional

#### 5) optional
        var _localStr: String?
        print("unwrapped-1 \(_localStr)")  ==> Compile OK,
        ==> Output: unwrapped-1 nil
#### 6) optional
        var _localStr: String?
        _localStr = "ABC"
        print("_localStr \(_localStr)")    ==> Compile OK, 
        ==> Output: _localStr Optional("ABC")
#### 7) optional
        var _localStr: String?
        _localStr = "ABC"
        print("_localStr \(_localStr!)")    ==> Compile OK, forced unwrap
        ==> Output: _localStr ABC

#### 8) optional
        var _localStr: String?
        print("unwrapped-1 \(_localStr!)") ==> Compile OK. forced unwrap
        ==> Runtime crash
#### 9) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr?.characters.count
        print("_localStr \(_localStr!), length \(_strLen)")  
        ==> Output: _localStr ABC, length Optional(3)
#### 10) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr.characters.count  ==> Compile error: not upwrapped
#### 11) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr?.characters.count
        print("_localStr \(_localStr!), length \(_strLen!)")
        ==> Output: _localStr ABC, length 3
#### 12) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr!.characters.count
        print("_localStr \(_localStr!), length \(_strLen!)")  ==> Compile error: forced unwrapping non-optional value

#### 13) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr!.characters.count
        print("_localStr \(_localStr!), length \(_strLen)")
        ==> Output: _localStr ABC, length 3
#### 14) optional
        var _localStr: String?
        _localStr = "ABC"
        let _strLen = _localStr!.characters.count
        print("_localStr \(_localStr!), length \(_strLen?)")  ==> Compile error: forced optional chaining non-optional value