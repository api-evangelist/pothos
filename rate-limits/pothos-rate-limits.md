# Pothos Rate Limits

Pothos GraphQL is a client-side TypeScript library. It runs entirely within the developer's application process and does not make network requests to any Pothos-operated service. As a result, Pothos itself imposes no rate limits.

## Runtime Behavior

- Pothos adds zero runtime overhead to schema construction.
- All type resolution happens at TypeScript compile time.
- No telemetry, licensing checks, or external API calls are made at runtime.

## GraphQL Server Rate Limiting

Rate limiting for a Pothos-built API is the responsibility of the GraphQL server layer (e.g., GraphQL Yoga, Apollo Server, Mercurius) and any infrastructure in front of it (reverse proxies, API gateways, CDN edge rules).

### Common Approaches

| Layer | Tool / Pattern |
|---|---|
| Query complexity | `@pothos/plugin-complexity` — budget-based query cost analysis |
| Depth limiting | Custom complexity rules or `graphql-depth-limit` |
| Request rate limiting | HTTP middleware (e.g., `express-rate-limit`, Nginx `limit_req`) |
| Persisted queries | Allowlist of known query hashes |

## Plugin: Complexity

The `@pothos/plugin-complexity` plugin lets schema authors annotate fields with a cost value and enforce a maximum complexity budget per request before execution begins. This is the primary mechanism for preventing expensive queries from overloading a Pothos-powered API.

See https://pothos-graphql.dev/docs/plugins/complexity for configuration details.
