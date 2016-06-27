# Using with Phoenix

* In your `mix.exs`, add Elixirscript to you deps
  * ```elixir
     defp deps do
    [
     #other deps
     {:elixir_script, "~> 0.20.0"}
     ]
  end
  ```
* Also in your `mix.exs`, update the compilers key in the project
  * `compilers: [:phoenix, :gettext, :elixir_script] ++ Mix.compilers`