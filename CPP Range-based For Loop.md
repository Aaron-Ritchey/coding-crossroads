#languages/CPP #concepts/loops/foreach

Here's a quick code chunk for a foreach loop in C++.

**NOTE:** the double ampersand is *not* a typo

```c++
int[] array = [1,2,3,4,5];
for (auto&& element : array) {
    cout << element << "\n";
}
> 1
> 2
> 3
> 4
> 5
```
## Double Ampersand
> 🌈🌈 ...what does it mean?

(While I couldn't resist the meme, TBH, I'm still learning about [[CPP LValue and RValue]] so this section is incomplete.)

| code | meaning |
| ---- | ---- |
| `auto element : array` | **Access by Value**<br>Assign a *copy* of each array element to `num`. We can't edit `array`.  |
| `auto& element : array` | **Access by CONST Reference**<br>We get a reference to the value, so we *could* edit the `array`. |
| `auto&& element : array` | **Access by Forwarding Reference**<br>We ...also get a reference to the value? |
The documentation\[1] says that "*it is \[safe and preferable] to use \[&&\].*"

And supposedly in simple cases, compilers can optimize in simple cases so it won't matter whether you use `auto` or `auto&` or `auto&&`.

In all cases of `auto` or `auto&` or `auto&&`, the `auto` says "*define `num` as whatever type `num` is*".

## Read More
- \[1] [Range-based for loop - C++ Docs](https://en.cppreference.com/w/cpp/language/range-for)
- [Forwarding References - C++ Docs](https://en.cppreference.com/w/cpp/language/reference#Forwarding_references)