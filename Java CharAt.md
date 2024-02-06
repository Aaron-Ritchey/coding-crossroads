#languages/Java #concepts/string/char_at

Java won't let you treat the `String` as an array. You have to specifically ask for a character.

```java
int x = "tacocat".charAt(3);
> 'o'
```