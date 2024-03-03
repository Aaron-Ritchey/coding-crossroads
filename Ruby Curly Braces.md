#languages/Ruby 

Ruby is one of the "non curly brace" languages

```ruby
if (x > 5) then
	puts "success!"
end
```

Yet it also has curly braces in some cases

```ruby
nums.each { |x|
	if (x > 5) then
		puts "success!"
	end
}

nums.each do |x|
	if (x > 5) then
		puts "success!"
	end
end
```