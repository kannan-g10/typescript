# TypeScript Syllabus — 0 to Advanced

**Prereqs:** Solid JS (ES6+, functions, objects, arrays, promises/async).
**Format:** Learn → Build → Checkpoint per module. 1-2 modules/week.

---

## Module 0: Why TypeScript & Setup
- [ ] Install: `npm install -g typescript`, `tsc --init`
- [ ] `tsconfig.json` key options: `strict`, `target`, `module`, `outDir`
- [ ] Compile a `.ts` file, understand type erasure (compiles to plain JS)
- [ ] ts-node or tsx for running directly
- **Checkpoint:** Explain in one line why TS catches bugs JS can't.

## Module 1: Basic Types
- [ ] Primitives: `string`, `number`, `boolean`, `null`, `undefined`
- [ ] Arrays, tuples
- [ ] `any` vs `unknown` (and why avoid `any`)
- [ ] Type inference vs explicit annotation
- [ ] `enum`, `literal types`
- **Build:** Type a small CLI script (e.g., expense calculator) fully — no `any`.
- **Checkpoint:** Convert 5 untyped JS snippets to properly typed TS.

## Module 2: Functions
- [ ] Parameter/return types, optional (`?`) and default params
- [ ] Rest params, function overloads
- [ ] `void`, `never` return types
- [ ] Arrow functions with types
- **Build:** Typed utility functions library (sum, groupBy, debounce) with overloads where useful.
- **Checkpoint:** Write a function overload that behaves differently based on input type.

## Module 3: Objects & Interfaces
- [ ] `interface` vs `type` — when to use which
- [ ] Optional properties, readonly properties
- [ ] Extending interfaces, intersection types (`&`)
- [ ] Index signatures
- **Build:** Model a domain (e.g., stock portfolio: `Holding`, `Transaction`, `Portfolio`).
- **Checkpoint:** Explain interface merging vs type alias limitations.

## Module 4: Union Types & Narrowing
- [ ] Union types (`|`), discriminated unions
- [ ] Type narrowing: `typeof`, `instanceof`, `in`, custom type guards
- [ ] `switch` narrowing on discriminated unions
- [ ] Exhaustiveness checking with `never`
- **Build:** Model API response states: `Loading | Success<T> | Error` and handle exhaustively.
- **Checkpoint:** Add a new variant to a discriminated union, let the compiler catch unhandled cases.

## Module 5: Generics
- [ ] Generic functions, generic interfaces/types
- [ ] Constraints (`extends`), default type params
- [ ] Generic classes
- [ ] Common patterns: `Array<T>`, `Promise<T>`, custom `Result<T, E>`
- **Build:** Generic `fetchData<T>()` wrapper + a generic `Stack<T>`/`Queue<T>` class.
- **Checkpoint:** Write a generic function constrained to objects with an `id` field.

## Module 6: Advanced Object Types
- [ ] Utility types: `Partial`, `Pick`, `Omit`, `Required`, `Readonly`, `Record`
- [ ] `keyof`, `typeof` operators
- [ ] Mapped types (build your own utility type)
- [ ] Conditional types (`T extends U ? X : Y`)
- [ ] Template literal types
- **Build:** Build a custom `DeepPartial<T>` and `DeepReadonly<T>` from scratch.
- **Checkpoint:** Explain how `Pick` is implemented internally (mapped + keyof).

## Module 7: Classes & OOP in TS
- [ ] Access modifiers: `public`, `private`, `protected`
- [ ] Abstract classes, interfaces implementation
- [ ] Static members, getters/setters
- [ ] Decorators (basics — used heavily in NestJS/Angular)
- **Build:** Small class hierarchy (e.g., `Shape` → `Circle`, `Rectangle` with abstract `area()`).
- **Checkpoint:** Explain `private` (TS-only, erased) vs `#field` (real JS private).

## Module 8: Modules & Project Structure
- [ ] ES module import/export with types
- [ ] `import type` vs regular import
- [ ] Declaration files (`.d.ts`), `declare module`
- [ ] Path aliases in `tsconfig.json`
- **Build:** Multi-file project with barrel exports and path aliases.
- **Checkpoint:** Write a `.d.ts` file for a small untyped JS library.

## Module 9: Working with External Libraries
- [ ] `@types/*` packages, DefinitelyTyped
- [ ] Typing third-party libraries without types
- [ ] Typing API responses (Zod for runtime validation + inferred types)
- [ ] Typing environment variables safely
- **Build:** Add Zod validation to an API call, infer TS types from the Zod schema (`z.infer`).
- **Checkpoint:** Explain why runtime validation (Zod) matters even with TS types (TS is compile-time only).

## Module 10: TypeScript with React/Next.js
- [ ] Typing props, state, hooks (`useState<T>`, `useRef<T>`)
- [ ] Typing event handlers
- [ ] Typing children, `React.FC` vs explicit return type (why avoid `React.FC`)
- [ ] Generic components
- **Build:** Fully typed reusable `<Table<T>>` component (generic over row data).
- **Checkpoint:** Type a custom hook that returns a tuple like `useState`.

## Module 11: Advanced Type-Level Programming
- [ ] Recursive types
- [ ] Infer keyword in conditional types
- [ ] Variadic tuple types
- [ ] Branded/nominal types (for e.g. `UserId` vs `string`)
- **Build:** Type-safe event emitter (`on<K extends keyof Events>(event: K, cb: (payload: Events[K]) => void)`).
- **Checkpoint:** Build a branded type to prevent mixing up `UserId` and `OrderId` (both strings underneath).

## Module 12: Tooling & Best Practices
- [ ] `strict` mode flags explained individually (`strictNullChecks`, `noImplicitAny`, etc.)
- [ ] ESLint + `@typescript-eslint` setup
- [ ] Monorepo type-sharing (Turborepo/workspaces)
- [ ] Migrating a JS codebase to TS incrementally (`checkJs`, `allowJs`)
- **Build:** Take a small JS project and migrate it to TS incrementally.
- **Checkpoint:** List 5 strict flags and what bug class each one prevents.

## Capstone Project
Type a complete small application end-to-end with zero `any`:
- Domain models with discriminated unions
- Generic reusable utilities/components
- Zod-validated API layer with inferred types
- Branded types for IDs
- Strict mode fully enabled, ESLint clean

**Suggested capstone (fits your interests):** Typed expense/portfolio tracker backend — strict domain modeling for transactions, holdings, and API contracts.

---

## Resources
- Official handbook: typescriptlang.org/docs/handbook
- "Type Challenges" (GitHub repo) — for advanced type-level practice
- Matt Pocock's TS content (free) — sharp, practical, no fluff

## Time Estimate
- Fundamentals (0-4): ~3 weeks
- Intermediate (5-8): ~3 weeks
- Advanced (9-12) + Capstone: ~3-4 weeks
- **Total: ~9-10 weeks**
