# Basic Data Types

Below is a chart showing how each data type maps to JavaScript.

| Elixirscript | JavaScript |
| -- | -- |
| 1 | 1 |
| 1.123 | 1.123 |
| "Hello" | "Hello" |
| 'Hello' | 'Hello' |
| """multiline string""" | "multiline\nstring" |
| true | true |
| :atom | Symbol.for("atom") |
| [1, 2, 3] | Object.freeze([1, 2, 3]) |
| {1, 2, 3} | new Tuple(1, 2, 3) |
| %{one: 1, "two" => 2} | {[Symbol.for("one")]: 1, two: 2} |
| `PID<0.0.0>` | new PID() |
| `Reference<0.0.0.0>` | new Reference() |
| `<<1, 2, 3>>` | new BitString(BitString.integer(1), BitString.integer(2), BitString.integer(3)) |
