# Using with Phoenix

* In your `mix.exs`, add Elixirscript to you deps
  * ```elixir
     defp deps do
    [
     #other deps
     {:elixir_script, "~> 0.22.0"}
     ]
  end
  ```
* In your `mix.exs`, update the compilers key in your project config
  * `compilers: [:phoenix, :gettext, :elixir_script] ++ Mix.compilers`
* Also, add the `elixir_script` key
  * `elixir_script: [ input: "web/static/exjs", output: "web/static/js"]]`
* In `config/dev.exs`, update the `watchers` config to add `elixirscript.watch`
  * `watchers: [node: ["node_modules/brunch/bin/brunch", "watch", "--stdin"], mix: ["elixirscript.watch"]]`
* Create the folder `web/static/exjs`
  * `mkdir web/static/exjs`

Now whenever you are running the server in development mode, your `exjs` files in `web/static/exjs` will be compiled whenever there is a change. The compiled output will end up in `web/static/js`. From there, Brunch will compile the JavaScript as usual
