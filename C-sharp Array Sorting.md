#languages/C-sharp #concepts/array/sort  

C# favors sorting in-place.
## In-place Sort

Pass the *reference* of the array to the `Array` class `.Sort()` function.

```c#
// `values` could also come from an argument
int[] values = new int[] { 1, 0, 0, 4, 1, 8, 0 };

// CORRECT
Array.Sort(values);
// value = { 0, 0, 0, 1, 1, 4, 8 }

// WRONG -- Array.Sort() returns void
int[] wrong = Array.Sort(values);
> error CS0029: Cannot implicitly convert type 'void' to 'int'
```
## Sort into New Array

Clone the array (correctly) and sort the cloned array in-place.

```c#
// These could come from an argument
int[] original_values = new int[] { 1, 0, 0, 4, 1, 8, 0 };
string[] should_be_rwby = new string[] { "red", "white", "blue", "yellow" };

// CORRECT
int[] sorted_values = new int[original_values.Length];
Array.Copy(original_values, sorted_values, original_values.Length);
Array.Sort(sorted_values);
// original_value = { 1, 0, 0, 4, 1, 8, 0 }
// sortd_value = { 0, 0, 0, 1, 1, 4, 8 }
```
### Looks Right, But Wrong
Depending on what language you're coming from, it's easy to assume you're copying an array when instead you're copying a *reference* to an array.

Rather than error out, this mistake can introduce subtle bugs.

```C#
// WRONG -- this _isn't_ copying the array,
//   it's copying the _reference_ to the array.
string[] should_be_alpha = new string[should_be_rwby.Length];
Array.Sort(should_be_alpha);
// should_be_alpha = { "b", "r", "w", "y" } -- LOOKS GOOD TO ME

// EXCEPT...
// should_be_rwby = { "b", "r", "w", "y" } -- WILL CAUSE BUGS
```
## Read More
- [Array.Sort Method - .NET API](https://learn.microsoft.com/en-us/dotnet/api/system.array.sort?view=net-8.0)
- [Andrew Whitaker's Answer](https://stackoverflow.com/a/27198026) on Stack Overflow