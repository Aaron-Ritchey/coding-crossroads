#languages/C-sharp #structures/dictionary

```csharp
var dict = new Dictionary<char, int>();
var count = frequency.GetValueOrDefault(0);

// Unsafe, will Throw if not present.
$count_1 = frequency['x'];

// Safe
$count_2 = frequency.TryGetValue('x', out 0);
```
