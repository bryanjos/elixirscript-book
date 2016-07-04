# Output

Now that we have our first elixirscript file saved, let's compile it. Run the following command in the same directory as `app.exjs`

```bash
elixirscript . -o dist
```

This will find all `.exjs` files in the current directory, compile them to JavaScript files, and place them in the `dist` directory. When you look inside of `dist`, you will see something like this:

```bash
├── Elixir.App.js
├── Elixir.ElixirScript.Agent.js
├── Elixir.ElixirScript.Atom.js
├── Elixir.ElixirScript.Base.js
├── Elixir.ElixirScript.Bitwise.js
├── Elixir.ElixirScript.Collectable.js
├── Elixir.ElixirScript.Enumerable.js
├── Elixir.ElixirScript.Integer.js
├── Elixir.ElixirScript.JS.js
├── Elixir.ElixirScript.Kernel.js
├── Elixir.ElixirScript.Keyword.js
├── Elixir.ElixirScript.List.js
├── Elixir.ElixirScript.Macro.Env.js
├── Elixir.ElixirScript.Map.js
├── Elixir.ElixirScript.MapSet.js
├── Elixir.ElixirScript.Module.js
├── Elixir.ElixirScript.Process.js
├── Elixir.ElixirScript.Range.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.Atom.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.BitString.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.Float.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.Integer.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.L.Marker.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.List.js
├── Elixir.ElixirScript.String.Chars.DefImpl.Elixir.Tuple.js
├── Elixir.ElixirScript.String.Chars.DefImpl.js
├── Elixir.ElixirScript.String.Chars.js
├── Elixir.ElixirScript.String.js
├── Elixir.ElixirScript.Tuple.js
└── Elixir.js
```

Your compiled code is in `Elixir.App.js`. The rest are the compiled standard library files. Elixirscript creates a JavaScript file for each module in your application. Elixirscript targets ES2015 and uses ES Modules. You may need to use a tool such as [Babel](https://babeljs.io/) to transpile these files further into a format current browsers understand.
