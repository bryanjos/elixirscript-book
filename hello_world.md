# Chapter 2: Hello World

Now that Elixirscript is installed, let's write a small program. Create a file named `app.exjs` and put the following into it:

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

Next, run the following command in the same directory

```bash
elixirscript . -o dist
```

This will find all `.exjs` files in the current directory, compile them to JavaScript files, and place them in the `dist` directory. When you look at this directory, you will see your compiled file (as `Elixir.App.js`) along with some other JavaScript files. These files represent the standard library for Elixirscript. Elixirscript targets ES2015 and uses ES Modules. You may have to use a tool such as [Babel](https://babeljs.io/) to transpile these files further into a format current browsers understand. Elixirscript will create a js file per module as well as one per protocol and protocol implementation.