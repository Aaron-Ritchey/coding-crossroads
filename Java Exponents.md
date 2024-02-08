#languages/Java #concepts/math/exponent

Java does not have an operator for exponent.

Furthermore, it's not in the standard library, you have to use `Math`.

And to add insult to injury, you need to coerce an integer raised to a power back into an integer.

```java
int x = 5;
int y = 3;
int answer = (int)(Math.pow(x, y));
> answer = 125
```