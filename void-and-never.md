# Void and Never

The "void" and "never" values are typically used as return types from functions.

## void

```typescript
// void indicates that a function returns with no value

function greet(name: string): void {
  console.log(`Hello ${name}`);
}
```

## never

```typescript
// never indicates that a function never returns

function fail(): never {
  throw 'Error!';
}

function infinite(): never {
  for await (const request of server) {
    req.respond({ body: "Hello World\n" });
  }
}
```

[< Previous](any-and-unknown.md) | [Next >](enum.md)
