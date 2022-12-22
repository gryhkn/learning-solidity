# Lesson 3: Functions and Modifiers in Solidity

In this lesson, we'll cover the following topics:

- Functions in Solidity
- Defining and calling functions
- Modifiers in Solidity
- Using modifiers to change the behavior of functions

## Functions in Solidity

Functions in Solidity are blocks of code that perform a specific task. You can define your own functions to perform any task you like. Here's the syntax for defining a function in Solidity:

`function functionName(input1Type input1Name, input2Type input2Name, ...) public/private/external returnType {
    // function body
}`

For example, here's a simple function that adds two numbers together and returns the result:

`function add(uint a, uint b) public returns (uint) {
    return a + b;
}`

## Defining and calling functions

To define a function, you'll need to specify the function's name, input parameters (if any), visibility (`public`, `private`, or `external`), and return type (if any). The function body is the code that will be executed when the function is called.

To call a function, you'll use the function's name followed by its input parameters (if any) in parentheses. For example:

`uint result = add(2, 3);`

## Modifiers in Solidity

Modifiers in Solidity are blocks of code that can be used to change the behavior of functions. You can define your own modifiers or use one of the many built-in modifiers provided by Solidity.

Here's the syntax for defining a modifier:

`modifier modifierName(input1Type input1Name, input2Type input2Name, ...) {
    // modifier body
}`
Here's an example of a simple modifier that checks if a caller is the contract owner:

`modifier onlyOwner {
    require(msg.sender == owner);
    _;
}`

## Using modifiers to change the behavior of functions

To use a modifier, you can apply it to a function by using the `modifierName` keyword before the function's name. For example:

`function someFunction() public onlyOwner {
    // function body
}`
This will cause the `onlyOwner` modifier to be executed before the `someFunction` function is called. If the caller is not the contract owner, the `require` statement will cause the function to revert. If the caller is the contract owner, the function will be executed as normal.
