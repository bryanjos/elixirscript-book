# Chapter 7: JavaScript Interop


Elixirscript, as of today, has a simple JavaScript interop story. **You should be able to interact with any JavaScript functions and data types without any impedance**.

Elixirscript does have an additional module for working with JavaScript, the `JS` module.

The `JS` module has macros for JavaScript functionality that may be useful, but fits outside of Elixirscript's focus on trying to be as close to idiomatic Elixir as possible.

More information and documentation on the JS module can be found [here](https://hexdocs.pm/elixir_script/ElixirScript.JS.html)

From this module, the macro that you will probably use the most is `import`. `JS.import` is how Elixirscript can import ES Modules. Let's take a small example. Assume we have a module and we want to import Ramda.

```elixir
defmodule MyModule do
    JS.import R, "ramda"

    def add(left, right) do
        R.add(left, right)
    end
end
```

`JS.import` translates into an ES module `import` statement. The first argument to `JS.import` is the alias you want the import module to have. In our example, we import Ramda as `R`. The second argument is the path to the module. It translates into something like this:

```JavaScript
import R from "ramda"
```
