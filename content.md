# Ruby Loops

> "You make a loop de loop and pull and your shoes are lookin' cool"

## Goals

By the end of this lesson you’ll be able to:

- Use assignment operators to update variable values
- Work with number and letter ranges using `..` and `...`
- Convert ranges to arrays with `to_a`
- Write and understand different loop types (`loop`, `while`, `until`, `for`, `times`)
- Pick the most readable loop for a task
- Combine loops with assignment to build small programs

<div class="alert alert-info">
  <ul>
    <li><a href="https://www.youtube.com/watch?v=vVATMe9XDdA">Video (with Amanda)</a></li>
    <li><a href="https://www.youtube.com/watch?v=ftq_subpJ40">Video (with Benny)</a></li>
    <li><a href="https://www.youtube.com/watch?v=Ezk1WWkMVmo">Video (with Aldo)</a></li>
  </ul>
</div>

## Review

### Assignment Operators

Assignment operators let you update variables without retyping the variable name.

```ruby
a = 1
a += 3   # add 3
puts a   # => 4

b = 4
b -= 2   # subtract 2
puts b   # => 2

num = 12
num *= 2 # multiply by 2
puts num # => 24

num /= 4 # divide by 4
puts num # => 6
```
{: .repl }

<aside class="tip">
  Think of <code>+=</code> as "take the old value and add this to it."
</aside>

### Ranges

Ranges in Ruby represent a sequence.

```ruby
puts (1..5).to_a     # => [1, 2, 3, 4, 5]
puts (1...5).to_a    # => [1, 2, 3, 4]
puts ('a'..'d').to_a # => ["a", "b", "c", "d"]
```
{: .repl }

## Loop Types

### 1. `loop do`

`loop do` is the simplest loop in ruby. Any code you put inside the `do..end` block will run until you hit the `break` keyword.

```ruby
i = 0
loop do
  puts "i is #{i}"
  i += 1
  break if i == 10
end
```
{: .repl }

<aside class="tip">
  You won't see this type of loop used much in Ruby. If you find yourself using <code>loop do</code>, know that there is probably a better loop for you out there.
</aside>

### 2. `while` loop

`while` loops rely on a condition. They are kind of like an `if` condition, but they run the code inside `do...end` while the condition is `true`.

```ruby
i = 0
while i < 5 do
  puts "i is #{i}"
  i += 1
end
```
{: .repl }

```ruby
guess = ""

while guess != "ruby" do
  puts "Guess the secret word:"
  guess = gets.chomp
end

puts "You got it!"
```
{: .repl }

### The `until` loop

The `until` loop is the opposite of the while loop. A while loop continues for as long as the condition is true, whereas an `until` loop continues for as long as the condition is false.

```ruby
i = 0
until i >= 10 do
 puts "i is #{i}"
 i += 1
end
```
{: .repl }

### The `for` loop

A `for` loop is used to iterate through a collection of information such as an array or range.

```ruby
for i in 0..5
  puts "#{i} zombies incoming!"
end
```
{: .repl }

### The `times` loop

The `times` loop is a nice feature of Ruby. Since integers (like `5`) are objects, we can call the `times` method and loop through that many times. `5.times` means: "run this block 5 times."

```ruby
5.times do
  puts "Hello, world!"
end
```
{: .repl }

In this loop, the `|number|` part is called a *block parameter*. On each iteration, Ruby passes the current iteration index (starting at 0) into the block parameter.

```ruby
5.times do |number|
  puts "Alternative fact number #{number}"
end
```
{: .repl }

## Project: Loops

In this project, you will write Ruby programs that leverage loops. This project includes automated tests, so click this link to get started <https://github.com/dpi-tta-projects/ruby-loops/fork>, fork the repository and create a codespace.

<aside class="warning">
  In order to get credit for completing this project you'll need to open the assignment link from canvas to generate an access token.
</aside>

## References

- [Learn Ruby: Looping with Ruby Cheatsheet | Codecademy](https://www.codecademy.com/learn/learn-ruby/modules/learn-ruby-looping-with-ruby-u/cheatsheet)
- [Loops | The Odin Project](https://www.theodinproject.com/lessons/ruby-loops)
