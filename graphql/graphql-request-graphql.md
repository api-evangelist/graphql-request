# GraphQL Request GraphQL API

GraphQL Request (now evolved into **Graffle**) is a minimal, isomorphic GraphQL client library for JavaScript and TypeScript. It does not expose a hosted GraphQL endpoint of its own — instead, it is a client-side tool used to send GraphQL queries to any external GraphQL API endpoint you configure. The library supports HTTP and in-memory (schema-direct) transports, custom scalars, file uploads via the GraphQL Multipart Request spec, a composable extension system (anyware/middleware), and full TypeScript type inference for queries, mutations, and subscriptions.

**Endpoint:** N/A - library/tooling, no hosted endpoint

**Documentation:** https://graffle.js.org/guides/getting-started

The SDL schema file (`graphql-request-schema.graphql`) in this directory documents the core data types, input types, and enumerations that make up the library's request/response contract and configuration surface:

- `GraphQLRequest` / `RequestInput` — the shape of a request sent to a GraphQL endpoint (query string, variables, operation name, operation type)
- `ExecutionResult` / `GraffleExecutionResultEnvelope` — the shape of a response, covering `data`, `errors`, and `extensions`
- `GraphQLError` / `GraphQLFormattedError` — error objects returned in execution results
- `OutputConfiguration` — controls whether errors throw or are returned, and whether an envelope is used
- `TransportHttpConfiguration` — HTTP transport settings (URL, method mode, headers)
- `VariablesMap` — key/value pairs of runtime GraphQL variable values
- `MethodMode` enum — `post` (JSON body, per GraphQL-over-HTTP POST spec) or `getReads` (URL search params, per GET spec)
- `OutputChannel` enum — `throw` or `return`
- `OperationType` enum — `query`, `mutation`, `subscription`

**References:**
- Documentation: https://graffle.js.org/guides/getting-started
- GitHub: https://github.com/graffle-js/graffle
- npm: https://www.npmjs.com/package/graphql-request
- GraphQL over HTTP spec: https://graphql.github.io/graphql-over-http/
- GraphQL Multipart Request spec: https://github.com/jaydenseric/graphql-multipart-request-spec
