Every language has as `stack`. Some languages have different behaviors.

- Push Behavior
	- In Python3 you `append`.
- Peek Behavior
	- In Python3 there is not `peek`, you check the last element with `array[-1]`.
		- See also [[Pet Peeve of Lacking Negative Indexing]]
- Pop Behavior
	- In Python3 the `pop` function returns the last element.
	- In C++, the `pop_back` function returns *nothing*.
- In PHP
	- You call a function and pass it an array and a value.
		- `array_push($array, $value)`
	- Most other languages attach the `push` to the Array itself.