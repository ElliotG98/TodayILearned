# Barrels

A barrel is a way to rollup exports from different modules into one convenient module. The barrel is a module file which imports the modules itself and re-exports as a single module.

As an example, take a landing page. We may have imports such as:
```ts
    import {Hero} from './containers/Hero'
    import {About} from './containers/About'
    import {contanctForm} from './containers/ContactForm'
```

We could use a barrel within the containers folder to consolodate this into a one liner.

Create an `index.ts` file within the containers directory and export all of the modules.

```ts
    export * from './Hero'
    export * from './About'
    export * from './ContactForm'
```

Now in our landing page we can import them all as a one liner.

```ts
    import { Hero, About, ContactForm } from './containers'
```

Thats how we use barrels in typescript/javascript to clean up our imports.
