# TypeScript Compiler Options
TypeScript compiler options can be specified on the command-line or in a configuration file.

## Compile using command-line options
The following command does not use the `ts-config.json` file.
```shell
$ npx tsc --outDir dist mylib.ts myclient.ts
```
See the command-line options here: <a href="https://www.typescriptlang.org/docs/handbook/compiler-options.html" target="_blank">https://www.typescriptlang.org/docs/handbook/compiler-options.html</a>

## Compile using `ts-config.json`
A `ts-config.json` file...
* Indicates the root directory of a TypeScript project
* Specifies the files and compiler options required to build the project
* Is used when the compiler is run without specifying any input files or the `--project` option is provided with the path to the configuration file

A new TypeScript project is typically started by creating a fully documented `ts-config.json` file like this:
```shell
$ npx tsc --init
```

See the ts-config reference here: <a href="https://www.typescriptlang.org/tsconfig" target="_blank">https://www.typescriptlang.org/tsconfig</a>

When the `npx tsc` command is run...
* The compiler searches for `ts-config.json` first in the current directory and then up the directory tree
* By default, it compiles all `*.ts` files recursively starting from the root directory

Common `ts-config.json` settings include:
* `files` - static list of files to be compiled
* `include` - dynamic list of files to be compiled (supports glob patterns like `src/**/*.ts`)
* `exclude` - dynamic list of files to be excluded from compilation (supports glob patterns)

[< Previous](playground.md) | [Next >](type-declaration-files.md)
