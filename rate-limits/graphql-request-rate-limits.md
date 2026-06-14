# GraphQL Request Rate Limits

GraphQL Request (Graffle) is a client-side library and does not itself impose any rate limits. Rate limiting is determined entirely by the GraphQL API server the library connects to.

## Client Library Behavior

- No built-in rate limiting logic in the library
- No request throttling by default
- No quota enforcement at the library level
- The library sends requests as fast as the calling code instructs

## Server-Side Rate Limits

When using graphql-request / Graffle to call a third-party GraphQL API, you are subject to that API's rate limits. Common patterns include:

- **Request-per-minute limits** — enforced by the GraphQL server (e.g., GitHub GraphQL API: 5,000 points/hour)
- **Complexity-based limits** — some servers limit by query complexity score rather than raw request count
- **Concurrent connection limits** — depends on the target server configuration

## Implementing Rate Limit Handling in Your Application

Since the library has no built-in rate limit handling, you must implement this in your application code:

- Use the `retry` extension or wrap calls with a retry library (e.g., `p-retry`)
- Inspect HTTP response headers (e.g., `X-RateLimit-Remaining`, `Retry-After`) returned by the target API
- Implement exponential backoff for `429 Too Many Requests` responses
- Use the Graffle extension system to add custom request middleware for rate limit awareness

## References

- Graffle Extension System: https://graffle.js.org/extensions
- GraphQL over HTTP Spec: https://graphql.github.io/graphql-over-http/
