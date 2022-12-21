# Lesson 2: Data Types and Variables in Solidity

In this lesson, we'll cover the following topics:

- Data types in Solidity
- Declaring variables
- Assigning values to variables
- The memory and storage keywords

## Data types in Solidity

Solidity has a number of built-in data types that can be used to represent different kinds of values. Here are some of the most common data types in Solidity:

- bool: A boolean value (true or false)
- int: A signed integer
- uint: An unsigned integer
- bytes: A dynamically-sized byte array
- string: A dynamically-sized string
- address: An Ethereum address

You can also define your own data types using structs and enums.

## Declaring variables

To use a variable in Solidity, you first need to declare it. Here's how you declare a variable in Solidity:

`dataType varName;`

For example:

`uint myNumber;
bool myBoolean;`

## Assigning values to variables

You can assign a value to a variable when you declare it, like this:

`uint myNumber = 42;
bool myBoolean = true;`

Or you can assign a value to a variable after you've declared it using the assignment operator =, like this:

`myNumber = 42;
myBoolean = false;`

## The memory and storage keywords

In Solidity, variables can be stored in memory or storage. Memory is a temporary area of the EVM that is used to store values during contract execution. Storage is a more permanent area of the EVM where values are stored between contract executions.

By default, variables are stored in memory, but you can use the storage keyword to specify that a variable should be stored in storage instead.

Here's an example of declaring a variable in storage:

`uint public myNumber stored in storage;`

You can also use the memory keyword to specify that a variable should be stored in memory, but this is not typically necessary since variables are stored in memory by default.
