# Basic Types

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
let name: string = 'Elon'; // single or double quotes

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
```

[< Previous](playground.md) | [Next >](any-and-unknown.md)
