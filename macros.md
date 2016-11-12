# Chapter 6: Macros

Elixirscript supports implementing public macros within your Elixirscript files. Let's look at an example.

```elixir
defmodule App do
  defmacro square(x) do
    quote do
      unquote(x) * unquote(x)
    end
  end

  def do_it(x) do
    square(x)
  end
end
```

Elixirscript will be able to expand the macro before compiling it to JavaScript.

`defmacrop` is not supported at this time.