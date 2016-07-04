# Chapter 4: Pattern Matching

Elixirscript supports **all** of the same pattern matching and guard rules that Elixir supports. Pattern Matching also works on JavaScript objects and classes as well.

Let's show an example of Pattern Matching on a JavaScript object. Assume we have a function, `process`, that takes a DOM element as a parameter. We want to process a div element with the id "my-div" differently so we will create a function head that matches just for it and another to match on all other elements.


```elixir

def process(%HTMLDivElement{id: "my-div"} = div) do

end

def process(element) do

end

````

As you can see, matching on JavaScript objects is similar to matching on structs.
