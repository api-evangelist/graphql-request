# GraphQL Request FinOps

GraphQL Request (Graffle) is a free, open-source library with no licensing costs. FinOps considerations relate to infrastructure and operational costs in your own environment, not library fees.

## Direct Costs

| Cost Item | Amount |
|-----------|--------|
| Library license | Free (MIT) |
| npm package download | Free |
| Software updates | Free |

## Indirect / Operational Cost Considerations

### Compute
- Minimal CPU and memory overhead; the library is lightweight (< 1 KB gzipped for legacy graphql-request)
- No significant compute cost attributable to the library itself

### Network / API Costs
- All network costs are driven by the GraphQL API endpoints you call, not the library
- If calling paid APIs (e.g., cloud vendor GraphQL endpoints), costs are billed by those providers
- AWS AppSync, Hasura Cloud, Apollo GraphOS, etc. each have their own pricing models

### Bundling
- For browser apps, bundle-size impact is minimal
- Tree-shaking compatible; unused extensions are not included in production bundles

### Observability
- The OpenTelemetry extension enables tracing of GraphQL requests, which may incur costs depending on your observability platform (e.g., Datadog, Honeycomb, New Relic)

## Cost Optimization Tips

- Use the in-memory transport for testing/development to eliminate network round-trips
- Cache GraphQL responses at the application layer to reduce redundant API calls to paid backends
- Leverage the extension system to add response caching without third-party dependencies
- Pin library versions to avoid unintentional breaking-change upgrades

## References

- npm: https://www.npmjs.com/package/graphql-request
- Graffle docs: https://graffle.js.org
- GitHub Sponsors (optional support): https://github.com/sponsors/jasonkuhrt
