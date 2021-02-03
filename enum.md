# TypeScript enum

TypeScript enums are compiled into JavaScript classes.

## Numeric values
```typescript
enum Color {
  RED = 1,
  GREEN,
  BLUE
}

const color: Color = Color.RED;

console.log(color);         // 1
console.log(Color["RED"]);  // 1
console.log(Color[1]);      // RED
```

Reverse mapping is implemented like this:

```javascript
"use strict";
var Color;
(function (Color) {
    Color[Color["RED"] = 1] = "RED";
    Color[Color["GREEN"] = 2] = "GREEN";
    Color[Color["BLUE"] = 3] = "BLUE";
})(Color || (Color = {}));
```

## String values
```typescript
enum Color {
  RED = 'red',
  GREEN = 'green',
  BLUE = 'blue'
}

const color: Color = Color.RED;

console.log(color);         // red
console.log(Color["RED"]);  // red
```

Since string values don't support reverse mapping so they are a little simpler:

```javascript
"use strict";
var Color;
(function (Color) {
    Color["RED"] = "red";
    Color["GREEN"] = "green";
    Color["BLUE"] = "blue";
})(Color || (Color = {}));
```

## Constant enums
TypeScript inlines enum values when declared as constant rather than create a JavaSript class.
```typescript
const enum Color {
  RED = 'red',
  GREEN = 'green',
  BLUE = 'blue'
}

const color: Color = Color.RED;
```
The constant enum above simply compiles to:
```javascript
"use strict";
const color = "red" /* RED */;
```
