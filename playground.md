# TypeScript Playground, TS Node, and Deno

The TypeScript Playground, TS Node, and Deno are useful tools for learning and running TypeScript programs.

## Playground

<a href="https://www.typescriptlang.org/play" target="_blank">https://www.typescriptlang.org/play</a>

* Test small TypeScript programs
* Export to other online editors
* Share code snippets with others
* View compiled JavaScript and type declarations

## TS Node

<a href="https://github.com/TypeStrong/ts-node" target="_blank">https://github.com/TypeStrong/ts-node</a>

* Run TypeScript code in Node without compiling
    ```shell
    $ npm init -y && npm install -D typescript
    $ npx ts-node myscript.ts
    ```
* Run as REPL
    ```shell
    $ npx ts-node
    > function greet(name: string): void {
    ... console.log(`Hello ${name}!`);
    ... }
    undefined
    > greet('Elon')
    Hello Elon!
    undefined
    > greet(1);
    [eval].ts:5:7 - error TS2345: Argument of type '1' is not assignable to parameter of type 'string'.
    ```    

## Deno

<a href="https://deno.land/">https://deno.land/</a>

Deno is a modern JavaScript runtime similar to Node.js but supports TypeScript out-of-the-box.

* Run TypeScript code in Deno without compiling
    ```shell
    $ deno run myscript.ts
    ```
* The Deno REPL does not yet support TypeScript

[< Previous](index.md) | [Next >](ts-config.md)
