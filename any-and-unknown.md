# Any and Unknown

The `any` and `unknown` types are similar in that TypeScript does not know their specific types but the compiler treats them very differently.

## any
```javascript
// "any" types can be assigned and re-assigned to any type
let value: any = 'Hello!';
value = 5;

value.toUpperCase(); // allowed but will fail at runtime
```

## unknown
```javascript
// like "any", "unknown" types can also be assigned and re-assigned to any type
let value: unknown = 5;
value = 'Hello';

value.toUpperCase(); // not allowed since TypeScript doesn't know if type supports toUpperCase()

// adding a type guard allows the value to be treated as a string
if (typeof value === 'string') {
  value.toUpperCase(); // allowed since TypeScript knows that it's a string here
}

// type assertion also allows value to be treated as a string
(value as string).toUpperCase();
```

[< Previous](undefined-and-null.md) | [Next >](any-and-unknown.md)
