#languages/PostgreSQL #concepts/string

Not sure if people took this knowledge for granted, but you wrap a string in single quotes. (Quite a shock I bet for people who see single quotes as defining a `char`.)

```postgresql

-- Great taste --
SELECT * FROM Movies WHERE director = 'Miyazaki'

-- Wrong syntax, but still great taste --
SELECT * FROM Movies WHERE director = "Miyazaki"
> 'column "Miyazaki" does not exist'

```