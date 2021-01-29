# Type Declaration Files

Type declaration files allow type information to be added to existing "untyped" JavaScript libraries.

## Add types to Lodash

1. Create Node project: `$ mkdir test && cd test && npm init -y`
1. Create TypeScript config file: `$ npx tsc --init`
1. Add Lodash dependency: `$ npm install lodash`
1. Create simple JavaScript file:
```javascript
// test.ts
import * as _ from 'lodash';

const text = "this is a test";
console.log(_.camelCase(text));
```
5. Load in VS Code: `$ code .`
1. Hover over "lodash" in the import and notice missing declaration file.
1. Type declaration files are available from <a href="https://definitelytyped.org/">Definitely Typed</a>.
1. Click "@types package search page" to search for a Lodash type file.
1. Install Lodash types: `npm install -D @types/lodash`
1. Missing declaration file warning is gone and code completion is available.
1. To run: `npx ts-node test.ts`

## Use existing types in Chalk

1. Add chalk dependency: `npm install chalk`
1. Update the test.ts file to use chalk:
```javascript
// test.ts
import * as _ from 'lodash';
import chalk from 'chalk';

const text = "this is a test";
console.log(chalk.blue(_.camelCase(text)));
```
3. Hover over chalk methods for docs or type "chalk." in editor to see code completion.
1. Run to see chalk in action: `$ npx ts-node test.ts`
1. Chalk is a JavaScript library that ships with a type declaration file (see `node_modules/chalk/index.d.ts`).

## Create a type declaration file

1. We'll distribute our own JavaScript library that includes type information.
1. Create a new project: `$ mkdir mylib && cd mylib && npm init -y && npx tsc --init`
1. Launch VS Code and create a new TypeScript file:
```javascript
// util.ts
export function add(x: number, y: number): number {
    return x + y;
}

export function subtract(x: number, y: number): number {
    return x - y;
}
```
4. Change "main" property in package.json to util.js and add “files” property:
```json
{
  "name": "mylib",
  "version": "1.0.0",
  "description": "",
  "main": "util.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "files": [
    "util.js",
    "util.d.ts"
  ]
}
```
5. Compile the TypeScript file and create a declaration file: `$ npx tsc --declaration util.ts`
1. Open "util.d.ts" to view the type declaration file.
1. Package for deployment: `$ npm pack`
1. Create client project: `$ cd .. && mkdir myclient && cd myclient && npm init -y`
1. Install library as dependency: `$ npm install ../mylib/mylib-1.0.0.tgz`
1. Launch VS Code: `$ code .`
1. Create the following JavaScript file:
```javascript
// test.js
import { add } from 'mylib';

const result = add(2, 3);

console.log(result);
```
12. Hover over the "add" method to see type information.
