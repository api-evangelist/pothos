# Pothos FinOps

Pothos GraphQL is a free, open-source library. Direct costs for using Pothos are zero. FinOps considerations apply to the surrounding infrastructure where a Pothos-built GraphQL API runs.

## Direct Costs

| Item | Cost |
|---|---|
| `@pothos/core` npm package | Free |
| All `@pothos/plugin-*` packages | Free |
| License (ISC) | Permissive; no royalties |

## Indirect Infrastructure Costs

These costs are incurred by the application hosting the GraphQL schema built with Pothos, not by Pothos itself.

### Compute

- GraphQL query execution runs in-process; compute cost scales with resolver complexity and concurrency.
- The `@pothos/plugin-complexity` plugin can cap per-request CPU/DB work, indirectly controlling compute spend.

### Database (Prisma / Drizzle Integration)

- The `@pothos/plugin-prisma` and `@pothos/plugin-drizzle` plugins enable direct ORM integration.
- N+1 query patterns are a common cost driver; use `@pothos/plugin-dataloader` to batch database calls and reduce round-trips.

### Dataloader Batching

- `@pothos/plugin-dataloader` batches and caches repeated field lookups within a single request, reducing database and downstream API call volume.

## Cost Optimization Patterns

| Pattern | Pothos Support |
|---|---|
| Query complexity budgets | `@pothos/plugin-complexity` |
| Batched data fetching | `@pothos/plugin-dataloader` |
| Persisted queries | Server-layer feature (e.g., GraphQL Yoga) |
| Sub-graph federation | `@pothos/plugin-federation` — split schema across services to scale independently |

## Sponsorship

If your organization derives value from Pothos, consider sponsoring the project at https://pothos-graphql.dev/docs/sponsors to support continued open-source development.
