# Pothos GraphQL API

Pothos is a TypeScript-first, code-first GraphQL schema builder library. It is not a hosted service with a network endpoint — it is an npm package that developers use to construct GraphQL schemas programmatically in TypeScript. The schema vocabulary documented here describes the types, directives, and patterns that Pothos generates and exposes when building a GraphQL API.

Pothos provides a plugin-based architecture with zero runtime overhead and no code generation required. Developers use the `SchemaBuilder` class to define all GraphQL types (Object, Interface, Union, Enum, Input, Scalar) and root operation types (Query, Mutation, Subscription), then call `builder.toSchema()` to produce a standard `graphql-js` schema.

**Endpoint:** N/A - library/tooling, no hosted endpoint

**Documentation:** https://pothos-graphql.dev/docs

**References:**
- Documentation: https://pothos-graphql.dev/docs
- GitHub: https://github.com/hayes/pothos
- NPM: https://www.npmjs.com/package/@pothos/core
- Discord: https://discord.gg/mNe73qvwAB
