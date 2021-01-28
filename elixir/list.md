# List on elixir

## Obs.:

Elixir list != Array

Example:

    iex(1)> a =[1,2,3,4]

you can't find array position,

    iex(2)>a[0]

    ** (ArgumentError) the Access calls for keywords expect the ke
    y to be an atom, got: 0
    (elixir 1.11.2) lib/access.ex:311: Access.get/3

## Keywords

    iex(1)> a = [first: 1, second: 2]
    [first: 1, second: 2]
    iex(2)>a[:first]
    1
