# Basic Types

TypeScript supports all of the standard JavaScript types plus several new ones.

```javascript
// boolean
let isDone: boolean = false;

// number
let decimal: number = 10;
let hex: number = 0xfa30b8;
let binary: number = 0b10110;
let octal: number = 0o755;
let big: bigint = 9999999n;

// string
let firstName: string = 'Elon';
let lastName: string = "Musk";

// array
let fruit: string[] = ['apple', 'orange', 'pear'];
let fruit: Array<string> = ['apple', 'orange', 'pear'];

// tuple
let student: [string, number] = ['Billy', 10];

// enum
enum Color {
  Red,
  Green,
  Blue,
}
let c: Color = Color.Green;

// undefined
let nothing: undefined = undefined;
nothing = 5; // not allowed, variable can only be assigned undefined

// null
let nothing: null = null;
nothing = 5; // not allowed, variable can only be assigned null

// The undefined and null types may seem pointless at first but we'll later see how they can be used in union types like this:
let firstName: string | undefined | null;
firstName = 'Elon'; // ok
firstName = undefined; // ok
firstName = null; // ok
```

[< Previous](type-declaration-files.md) | [Next >](any-and-unknown.md)
