# Basic Types

TypeScript supports all of the standard JavaScript types plus several new ones.

```typescript
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

// object - any non-primitive value
let student: object = { name: 'Billy', age: 10 };
student = [ 'Billy', 10 ];  // ok, arrays are objects
student = () => 'Billy';    // ok, functions are objects
student = 'Billy';          // not allowed (primitive type)
student = 5;                // not allowed (primitive type)
student = true;             // not allowed (primitive type)
```

[< Previous](type-declaration-files.md) | [Next >](undefined-and-null.md)
