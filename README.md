# Elixir List Modification Bug

This repository demonstrates a common error when working with lists in Elixir: attempting to modify a list while iterating using `Enum.each`. Elixir lists are immutable, meaning that the operation `List.delete` doesn't change the original list, only creates a new list.  The original list passed to `Enum.each` remains unchanged. The example illustrates this behavior and shows a correction using Enum.filter.

## How to Reproduce

1. Clone this repository.
2. Run `iex bug.ex`.
3. Observe that the list remains unmodified, despite the `List.delete` call within the loop.

## Solution

The `bugSolution.ex` file provides a solution using `Enum.filter` to create a new list excluding the element to be removed.
