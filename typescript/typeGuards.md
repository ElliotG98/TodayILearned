# Type Guards

Type guards are a way to determine the type of a variable based on runtime checks.

Some examples:

- `typeof`: The `typeof` type guard can narrow down primitive types.
```ts
function isNumber(value:unknown): value is number {
    return typeof value === 'number'
}
```

- `instanceof`: The `instanceof` type guard can narrow down the class type.

```ts
class Car {}

function isCar(value:unknown): value is Car {
    return instanceof value === Car
}
```

- Custom Type Guards: You can create your own type guards by defining a function which returns a boolean and type predicate.