# Chapter 5: Protocols

Elixirscript supports both `defprotocol` and `defimpl` allowing one to create their own protocols as well as create implementations for exisiting ones. Elixirscript supports using JavaScript objects to implement protocols as well.

```elixir
defmodule App do
  defimpl String.Chars, for: HTMLDivElement do
    def to_string(%HTMLDivElement{ id: id  }) do
      id
    end
  end
end
```

With the above example, whenever `String.Chars.to_string` is called with a div as the parameter, it will output its id.