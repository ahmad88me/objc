# objc

## learned from Harvard Objective C class

In the .h file:
```
@interface Foo: NSObject{
  // instace variables
}
//declatations of methods
@end
```
* So `@interface` means class in Java
* Foo is the name of the class
* `:` means extends
* `NSObject` is a class in Foundation library

In the .m file:
```
@implementation Foo
// definitions of methods
@end
```

=========

* Adding `@class` to a method means static (can be called on the class level rather that instance level)
* The function `alloc` is quivalent to malloc in c or new in Java. 
```
Student *student = [Student alloc]; // objective c
Student student = new Student(); // Java
```
* What in objective c called "message passing" is what in Java is called "method calling"

========

In instance method the convension is to call the getters by the variable name while have the setters starts with "Set".
```
- (int)age; // getter method that returns an int
- (void)setAge;(int)age; // setter method that takes an int as an argument and returns nothing (void) 
```

