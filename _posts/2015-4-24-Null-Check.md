---
layout: post
title: How to check Empty String SAFELY
---


```objective-c
NSString *title;
...
if (title == nil || title.length == 0 ) 
	title = @"Something";
```

### About [NSNull null]

`[NSNull null]` is used in collections like NSArray and NSDictionary to add null object because they can't contain `nil`.

```objective-c
NSArray *container = [NSArray arrayWithObjects:[NSNull null], @"", nil];
...
for (NSString *title in container) {
	// title comes from collection
	if (title == (id)[NSNull null] || title.length == 0 ) 
		NSLog(@"Empty string");
}
```
