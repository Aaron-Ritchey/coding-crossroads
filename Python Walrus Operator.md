#languages/Python #concepts/variable/assignment

The Walrus Operator `::walrus::` is something only a few languages have.

From personal experience, I've met multiple experienced (and intelligent) people who criticized the usefulness of this rather than admit they didn't know about it. That said, please keep an open mind.

```python
## ...with "Walrus Operator"
if ((next_key := ord(key) % 32) != last_key):
	## Do something with `next_key`

## ...without the operator.
next_key = ord(key) % 32
if (next_key != last_key):
	## Do something with `next_key`

```