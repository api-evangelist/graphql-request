# GraphQL Request

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
