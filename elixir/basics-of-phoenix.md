# Basics of Phoenix Framework

## What is this?

Phoenix is ​​a web development framework written in the functional programming language Elixir. Phoenix uses a standard server-side model display controller.

## how to create a project

### 1-First check that the phoenix is ​​installed correctly

      # for >= v1.3
      mix phx.new --version

      # for < v1.3
      mix phoenix.new --version

#### If it returns a version for example 1.5.7, it is installed.

is not installed? Click <a href="./install-phoenix.md">here</a>.

### 2- Create project

     mix phx.new demo --live
     cd demo
     mix phx.server

!!! note that when installing run the phx.server mix in the terminal, it will report several errors related to postgress, it occurs because the bank is not installed or is not connected with the project

Not instaled? Click <a href="../postgresql/configure-postgresql.md">here</a>.

or

     mix phx.new demo --no-webpack --html

if the project is an api there is no need in the webpack for packaging

### 3-Understanding the structure of the project

the first detail is the existence of a folder called config,
either with database data, ports and data that are not uninteresting to be read by other devs. And an important detail, there is no model folder
