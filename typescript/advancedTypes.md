# Advanced Types

Advanced types allow you to create more complex and expressive types.

Some examples: 

- Union Types: A union type can be one of serveral types. Defined using the `|` pipe character.

```ts
type DateOrString = Date | string
```

- Intersection Types: An intersection type is the combination of multiple types into one. Defined using the `&` ampersand character.

```ts
type Foo = {n: number, y: string}
type Bar = {z: Date}
```

- Type Aliases: A type alias is used to create a new name for a type.

```ts
type Point = number
type Board = {x: Point, y: Point}
```

- Mapped Types: A mapped type allows you to create a new type by transforming an existing types properties. Defined using the `in` keyword.

```ts
type Readonly<T> = {readonly [K in keyof T]: T[K]}
```

- Conditional Types: A conditional type is used to determine a type based on a condition. Defined using a ternary operator and `extends` keyword.

```ts
type IsNumber<T> = T extends number ? true : false
```
