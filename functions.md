# Functions

Functions in Elixirscript are transpiled into pattern matching functions. Let's take our example from Chapter 2.

```elixir
defmodule App do

  def hello() do
    "Hello, World"
  end
  
  def hello(name) do
    "Hello, #{name}"
  end

end
```

Becomes

```JavaScript

const hello = Patterns.defmatch(
  Patterns.clause([], function(){ return "Hello, World" }),
  Patterns.clause([Patterns.variable()], function(name){ return "Hello, " + name })
  );


export default {
  hello
}
 ```
 
`def` functions are exported while `defp` functions are not.