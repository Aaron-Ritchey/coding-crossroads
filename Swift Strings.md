#languages/Swift #concepts/string 

Swift is one of those langauges with a `Character` type.

```swift
let word_1 = "Hai!";
print(word_1);
> "Hai!"

// This is a Character array.
var array = Array(word_1);
print(array);
> ["H", "a", "i", "!"]

array[0] = "B";
print(array);
> ["B", "a", "i", "!"]  

// This is a String again.
let word_2 = String(array);
print(word_2);
> "Bai!"
```