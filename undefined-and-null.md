# Undefined and Null

The "undefined" type represents a variable that hasn't been assigned and "null" indicates a variable that has been assigned to nothing.

## undefined

```typescript
// undefined
let nothing: undefined = undefined;
nothing = 5; // not allowed, variable can only be assigned to undefined
```

## null

```typescript
// null
let nothing: null = null;
nothing = 5; // not allowed, variable can only be assigned to null
```

## purpose
```typescript
// The undefined and null types may seem pointless at first but we'll later see how they can be used in union types like this:
let firstName: string | undefined | null;
firstName = 'Elon';     // ok
firstName = undefined;  // ok
firstName = null;       // ok
```

[< Previous](basic-types.md) | [Next >](any-and-unknown.md)
