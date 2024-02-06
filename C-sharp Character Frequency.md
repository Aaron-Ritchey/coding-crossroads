#languages/C-sharp #concepts/string/frequency

There is no built-in function.

Here's a code snippet based on a Stack Overflow solution, using [[C-sharp Dictionary]].

```csharp
// Get frequency of letters in a word.
var word = "abracadabra";
var frequency = new Dictionary<char, int>();
foreach (var letter in word) {
	frequency[letter] = frequency.GetValueOrDefault(letter) + 1;
}
```

Based on:
https://stackoverflow.com/a/75727959