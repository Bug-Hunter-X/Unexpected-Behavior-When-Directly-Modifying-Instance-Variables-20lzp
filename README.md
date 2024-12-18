# Ruby Bug: Unexpected Behavior When Directly Modifying Instance Variables

This repository demonstrates a common, yet subtle, error in Ruby: directly modifying instance variables using `instance_variable_set`. While functional, this practice circumvents the intended object-oriented design and can lead to maintenance problems and unexpected side effects.

The `bug.rb` file showcases the problematic code. The `bugSolution.rb` file demonstrates a better approach using accessor methods.

## How to Reproduce

1. Clone this repository.
2. Run `ruby bug.rb`.
3. Observe the output, which might be unexpected if you're unfamiliar with the issue.

## Solution

The preferred approach is to use accessor methods (`attr_accessor`, `attr_reader`, `attr_writer`) to interact with instance variables.  This enforces encapsulation, improves code readability and maintainability, and allows you to add logic (validation, logging, etc.) as needed without altering core object functionality.