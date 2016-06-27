# Chapter 6: Macros

Elixirscript supports macros, but they have to be defined in `.ex` files. Elixirscript's compiler will find all `.ex` files in the path, load them, and expand any macros called in your `.exjs` files. Let's look at an example.

If you have a file named `macros.ex` with the following:

```elixir
defmodule Macros do
  def square(x) do
    quote do
      unquote(x) * unquote(x)
    end
  end
end
```

And call it in a module you define in `app.exjs`:

```elixir
defmodule App do
  require Macros

  def do_it(x) do
    Macros.square(x)
  end
end
```

Then Elixirscript will be able to expand it before compiling it. Macros are defined in `.ex` files because they are actually Elixir macros. In this way, Elixirscript macros work like Clojurescript macros.