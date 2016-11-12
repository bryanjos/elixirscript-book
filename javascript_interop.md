# Chapter 7: JavaScript Interop

Elixirscript code can interact with JavaScript in a number of ways.

## Importing ES Modules

First is importing JavaScript ES Modules. To import an ES module for use within your module, use `JS.import`. In our example, we will import Ramda.

```elixir
defmodule MyModule do
    JS.import R, "ramda"

    def add(left, right) do
        R.add(left, right)
    end
end
```

`JS.import` takes 2 parameters. The first one is either an Atom or a list of Atoms. The second is the import path or name of the ES module to import. When a single Atom is used for the first parameter, the expression is compiled into a default import statement in JavaScript

```JavaScript
import R from "ramda"
```

If a list of Atoms are used:

```elixir
JS.import [add, map, reduce], "ramda"
```

Then it is transformed into the following import statement:

```JavaScript
import {add, map, reduce} from "ramda"
```

Going back to our very first example, notice that calling functions on an imported module is done in the very same way one would call any Elixir function.

## Global functions

In order to call functions in the global scope, you can either use `JS.global\1` to get a reference to the global object or get the global object, such as window, using the Erlang module syntax

Let's take an example of calling `alert`


```Elixir
#This
JS.global().alert("Hi")

# is equivalent to
:window.alert("Hi")
```

## Calling Elixirscript code in JavaScript

To call Elixirsscript code in JavaScript is as simple as importing the module in your JavaScript module and calling the functions.

```elixir
defmodule MyModule do

    def add(left, right) do
        left + right
    end
end
```

```JavaScript
import MyModule from 'path/to/compiled/elixirscript/module/app/Elixir.MyModule'
MyModule.add(2, 3)
```