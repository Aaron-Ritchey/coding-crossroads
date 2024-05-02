#languages/C-sharp #concepts/array/list #concepts/array/queue #concepts/array/stack 

A quick example of `List` and `Stack` and `Queue` from Problem 977.

```c#
Stack<int> neg_squared_values = new Stack<int>();
Queue<int> pos_squared_values = new Queue<int>();
  
foreach (var num in nums) {
	if (num < 0) {
		neg_squared_values.Push(num*num);
	} else {
		pos_squared_values.Enqueue(num*num);
	}
}
  
List<int> result = new List<int>();
  
while (neg_squared_values.Any() && pos_squared_values.Any()) {
	if (neg_squared_values.Peek() < pos_squared_values.Peek()) {
		result.Add(neg_squared_values.Pop());
	} else {
		result.Add(pos_squared_values.Dequeue());
	}
}
```