# Pothos

Pothos is a plugin-based GraphQL schema builder for TypeScript that makes building GraphQL schemas easy, fast, and enjoyable. The core library adds zero overhead at runtime and requires only GraphQL as a peer dependency.

Pothos is the most type-safe way to build GraphQL schemas in TypeScript. By leveraging type inference and TypeScript's powerful type system, Pothos requires very few manual type definitions and no code generation. It does not depend on experimental decorators.

Used in production at Airbnb, Netflix, and other large-scale organizations.

## Links

- **Website:** https://pothos-graphql.dev/
- **Documentation:** https://pothos-graphql.dev/docs
- **GitHub:** https://github.com/hayes/pothos
- **npm:** https://www.npmjs.com/package/@pothos/core
- **Discord:** https://discord.gg/mNe73qvwAB

## Key Features

- Code-first, type-safe schema construction — no code generation required
- Unique plugin system where every plugin feels native to the core API
- 16+ official plugins: Auth, Prisma, Drizzle, Relay, Dataloader, Validation, Errors, Tracing, Federation, and more
- Zero runtime overhead; works at every scale from prototypes to enterprise applications

## Plugins

| Plugin | Purpose |
|---|---|
| `@pothos/plugin-auth` | Field and type-level authorization |
| `@pothos/plugin-complexity` | Query complexity budgets |
| `@pothos/plugin-dataloader` | Batched/cached data fetching |
| `@pothos/plugin-drizzle` | Drizzle ORM integration |
| `@pothos/plugin-errors` | Typed error handling in schema |
| `@pothos/plugin-federation` | Apollo Federation support |
| `@pothos/plugin-prisma` | Prisma ORM integration |
| `@pothos/plugin-relay` | Relay-spec connections and nodes |
| `@pothos/plugin-simple-objects` | Lightweight object type helpers |
| `@pothos/plugin-validation` | Input validation via Zod/Yup |

## Repository Contents

```
apis.yml                        APIs.json 0.19 catalog entry
plans/pothos-plans.md           Licensing and plan information
rate-limits/pothos-rate-limits.md  Rate limiting guidance
finops/pothos-finops.md         FinOps and cost considerations
```

## Maintainer

Kin Lane — kin@apievangelist.com
