# Monkey 🐒

Monkey is a small programming language created by [Thorsten Ball](https://interpreterbook.com/) in _Writing an Interpreter in Go_.

This repository contains a Monkey interpreter written in Go.

## Features

Monkey currently supports:

- Integers
- Booleans
- Variables with `let`
- `return` statements
- Arithmetic and comparison operators
- `if` / `else` expressions
- Functions
- Function calls
- First-class functions

## Example

```monkey
let x = 10;
let y = 20;

let add = fn(a, b) {
    a + b;
};

let result = add(x, y);

if (result > 20) {
    result;
}
```

## Running

Start the Monkey REPL with:

```bash
go run .
```

Then try:

```text
>> let x = 5;
>> x + 10;
15

>> let double = fn(x) { x * 2; };
>> double(5);
10
```

## How It Works

The interpreter follows a simple pipeline:

```text
Source Code
    ↓
Lexer
    ↓
Parser
    ↓
AST
    ↓
Evaluator
    ↓
Result
```

The project is being built incrementally while following _Writing an Interpreter in Go_.

## Reference

Thorsten Ball — _Writing an Interpreter in Go_

https://interpreterbook.com/
