#languages/CPP #concepts/string/frequency 

See also [[CPP Iterate over String]]

```c++
// 0=a, 1=b, ..., 25=z
int tally[26];
for (char& c: source) {
  ++tally[c-97];
}
```