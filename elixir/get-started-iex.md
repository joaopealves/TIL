# Get Started Iex

Iex is an interactive CLI, can run this writing iex on console.

## Operators ➕ ➖ ✖ ➗

    5+5
      10

    5-5
      0

    5*5
      25

    5/5
      1.0

Wait, why, 1.0? A float? Yes, in the elixir when dividing using /, the value returns a float. To return an int you have to use div (num1, num2)

    div(5, 5)
      1

take division rest, you can use: rem(num1, num2)

    rem(5.2)
      1

## Atom

Constant, so that the value is immutable

    :example

## String

You can use "" to define strings

string = "STRING"

## Use variables on text

To use variables, try #{variable} or #{"Text"}

    string = "example"

    "see this #{string}"
      see this example
