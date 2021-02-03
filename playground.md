# TypeScript Playground and TS Node

The TypeScript Playground and TS Node are useful tools when learning and running TypeScript programs.

## Playground

<a href="https://www.typescriptlang.org/play" target="_blank">https://www.typescriptlang.org/play</a>

* Test small TypeScript programs
* Export to other online editors
* Share code snippets with others
* View compiled JavaScript and type declarations

## TS Node

<a href="https://github.com/TypeStrong/ts-node" target="_blank">https://github.com/TypeStrong/ts-node</a>

* Run TypeScript code in Node without compiling
    ```
    $ npx ts-node myscript.ts
    ```
* Run as REPL
    ```
    $ npx ts-node
    > function greet(name: string) {
    ... console.log(`Hello ${name}!`);
    ... }
    undefined
    > greet('Elon')
    Hello Elon!
    undefined
    > greet(1);
    [eval].ts:5:7 - error TS2345: Argument of type '1' is not assignable to parameter of type 'string'.
    ```    

[< Previous](index.md) | [Next >](ts-config.md)
