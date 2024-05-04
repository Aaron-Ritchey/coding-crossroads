#languages/Java #concepts/array/list #concepts/array/stack #concepts/array/queue 

Working with lists, stacks, and queues are tricky in Java. See the examples further below.
## Quick Reference
| Structure | Object | putting | getting | peeking |
| ---- | ---- | ---- | ---- | ---- |
| `Stack<T> x` | `new Stack<T>()` | push() | pop() | peek() |
| `Queue<T> x` | `new LinkedList<T>()` | add() | remove() | peek() |
| `List<T> x` | `new ArrayList<T>()` | add() |  |  |
## Example
```java
Stack<Integer> neg_squared_values = new Stack<Integer>();
Queue<Integer> pos_squared_values = new LinkedList<Integer>();

for (int num : nums) {
	if (num < 0) {
		neg_squared_values.push(num*num);
	} else {
		pos_squared_values.add(num*num);
	}
}
  
List<Integer> result = new ArrayList<Integer>();
  
while (!neg_squared_values.isEmpty() && !pos_squared_values.isEmpty()) {
	if (neg_squared_values.peek() < pos_squared_values.peek()) {
		result.add(neg_squared_values.pop());
	} else {
		result.add(pos_squared_values.remove());
	}
}
```