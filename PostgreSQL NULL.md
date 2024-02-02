#languages/PostgreSQL #concepts/null

`NULL` is not a normal value. It is neither truthy nor falsy.

> `NULL = NULL` is false.
> `NULL != NULL` is also(!) false.

To check if a value is `NULL`
> `NULL is NULL` is true.

https://www.percona.com/blog/handling-null-values-in-postgresql/