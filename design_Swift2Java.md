# Design: Swift 4 to Java 8 translation

Below is a list of proposals for translation of Swift 4 constructs into Java 8 equivalent counterparts, with focus on the less obvious cases. Since Java 8 makes available most, if not all of the JVM computational possibilities, the language itself can offer a proper notation for exploring how to implement Swift 4 constructs within JVM semantics.

In the future, this mapping should implemented throughout a formal, well-defined, injective application from the set of Swift formal semantics into the set of Java 8 semantics.

(This list is work in progress. It may be extended, shortened or modified at any time ;) )

## Variable and constant declarations

### Swift 4
```swift
let a = 8; // this is a constant...
var b = 5; // and this a variable. Types are inferred.
```
---
### Java 8
```java
final int a = 8; // this is a constant...
int b = 5; // and this a variable. Types are explicit.
```
---

## Global declarations
### Swift 4
```swift
let a = 8; // this is globally-scoped constant.
// This is a global function.
func orphanFhunction(name:String) {
   ...
}
```
---
### Java 8
```java
// A global class containing global declarations, since 
// in Java every non-class declaration must belong into a class (or
// lesser) scope.
public class Globals {
  public final static int a = 8;
  public final static void orphanFunction(final String name) {
    ...
  }
}
```
---

## Optional type declarations
### Swift 4
```swift
var optionalInteger: Int?
var anotherOptionalInteger: Optional<Int>
```
---
### Java 8
```java
Integer i = new Integer();
Optional<Integer> optionalInteger = Optional.of(i);
```
---

