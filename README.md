# GraphQL Request

Minimal, isomorphic GraphQL client for JavaScript/TypeScript originally created by the Prisma team. The library has evolved and is now published as [Graffle](https://graffle.js.org) (the `graphql-request` npm package legacy branch remains available). It supports file uploads, batch requests, custom headers, TypeScript type inference, and a powerful extension system. Runs in Node.js and all modern browsers.

## Overview

- **npm package:** `graphql-request` (legacy) / `graffle` (current)
- **GitHub:** https://github.com/graffle-js/graffle
- **Documentation:** https://graffle.js.org
- **License:** MIT
- **Stars:** 6,100+

## Key Features

- Minimal API surface — send a GraphQL query in two lines of code
- Full TypeScript type inference via Document Builder
- HTTP and in-memory transport support
- Composable extension system (OpenTelemetry, file uploads, schema error handling)
- Custom scalar codec support
- Spec-compliant with GraphQL over HTTP and GraphQL Multipart Request specifications

## Quick Start

```bash
npm install graphql-request graphql
```

```typescript
import { request, gql } from 'graphql-request'

const query = gql`
  {
    users {
      id
      name
    }
  }
`

const data = await request('https://api.example.com/graphql', query)
```

## Resources

| Resource | URL |
|----------|-----|
| Website | https://graffle.js.org |
| Documentation | https://graffle.js.org/guides/getting-started |
| GitHub | https://github.com/graffle-js/graffle |
| npm (current) | https://www.npmjs.com/package/graffle |
| npm (legacy) | https://www.npmjs.com/package/graphql-request |
| Sponsor | https://github.com/sponsors/jasonkuhrt |

## Catalog Files

- [apis.yml](apis.yml) — APIs.json 0.19 catalog entry
- [plans/graphql-request-plans.md](plans/graphql-request-plans.md) — Pricing and plan details
- [rate-limits/graphql-request-rate-limits.md](rate-limits/graphql-request-rate-limits.md) — Rate limiting guidance
- [finops/graphql-request-finops.md](finops/graphql-request-finops.md) — FinOps and cost considerations

## Maintainer

Kin Lane — kin@apievangelist.com
