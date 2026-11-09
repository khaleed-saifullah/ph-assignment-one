# Type Alias vs Interface in TypeScript

## Introduction

In TypeScript, both `type` and `interface` help us define the shape of data. They look similar, but they have some differences.

## Type Alias

A `type` lets us create a custom name for almost any type, including objects, unions, primitives, and more.

```ts
type User = {
  name: string;
  age: number;
};

type Status = "active" | "inactive";
```

## Interface

An `interface` is mainly used to describe the structure of objects. It can also be extended by other interfaces.

```ts
interface User {
  name: string;
  age: number;
}

interface Admin extends User {
  role: string;
}
```

## Key Differences

- `type` supports unions, intersections, and primitive types.
- `interface` is mainly focused on object structures.
- Both support extending or combining object types.
- Interfaces can be reopened and merged, while type aliases cannot.

## Conclusion

Both are useful and widely used in TypeScript. Use `interface` when defining object structures, and use `type` when you need unions or more flexible type combinations. Choose whichever makes your code easier to understand!
