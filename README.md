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

In instance method the convension is to call the getters by the variable name while have the setters starts with "set".
```
- (int)age; // getter method that returns an int
- (void)setAge;(int)age; // setter method that takes an int as an argument and returns nothing (void) 
```
setter and getter example:
```
[student age]; // call the getter method for the instance student to get the age 
[student setAge:20]; // call the setter method setAge and pass the parameter 20
```
initializing an object (calling a contructor like method)
```
[student init];// initializing the new object student
[student initWithName:@"Alice" andAge:20]; // Apple convension is to have the methods to be readable, so the first argument is @"Alice" and the second argument value is 20 and the second parameter name is "andAge"
```

=========
An example to declar a class object called Student
```
//in Student.h
#import <Foundation/Foundation.h>
@interface Student : NSObject{
@public
  int age;
  NSString *name;
}
@end
```
The main file:
```
//main.m
#import <Foundation/Foundation.h>
#import "Student.h"

void greet(Student *s);

int main(int argc, const char * argv[]){

  Student *alice = [Student alloc];
  alice->age = 20;
  alice->name = @"Alice";
  greet(alice);
  return 0;
}

```


