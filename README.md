# Console Group (console-group)

Console Group is an Australian property management software company, founded in 1992 in Brisbane, Queensland, that built the first property management and trust accounting software released in Australia and launched its cloud platform, Console Cloud, in 2017. It serves thousands of residential and commercial property management agencies across Australia and New Zealand with trust accounting, tenancy and lease management, inspections (Console Go + Inspect), maintenance, arrears, owner and tenant portals, SMS, analytics and payments (Console Pay). The company was acquired by the United Kingdom's Reapit and its flagship product has been rebranded Reapit PM, though the business continues to trade from console.com.au. In the Australian value chain Console Group sits on the property MANAGEMENT side rather than the sales-listing side, as the system of record for the rent roll, the trust account and the tenancy, downstream of REA Group's realestate.com.au and Domain and separate from PEXA's conveyancing rail and from PropTrack and CoreLogic valuation data. Its API posture is honestly closed. Console Group publishes no developer portal, no API reference, no OpenAPI or Swagger document and no partner developer program on console.com.au; the full sitemap contains no /developers, /api or /docs page, and the developer., developers. and docs. subdomains do not resolve. An api.console.com.au host answers as a Kong API Gateway (`{"message":"no Route matched with those values"}`) but exposes no route on any probed path. A live integration marketplace at /integrate lists more than twenty two-way third-party products, so a working private integration API demonstrably exists, but access is by commercial marketplace arrangement only and nothing about it is published. Australia has no MLS, so there is no RESO Web API or Data Dictionary certification, no OData `$metadata` document and no Universal Property Identifier anywhere in Console Group's stack, and the company publishes no open data.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/console-group/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/console-group/refs/heads/main/apis.yml)

## Tags

- Real Estate
- Australia
- New Zealand
- Property Management
- PropTech
- Trust Accounting
- Rentals
- Tenancy
- Commercial Real Estate
- Inspections
- Payments

## Timestamps

- **Created:** 2026-07-26
- **Modified:** 2026-07-26

## APIs

No public, documented APIs are listed for Console Group.

This is a finding, not a gap in the research. Console Group publishes no developer
portal, no API reference and no machine-readable contract of any kind. The following
were probed anonymously on 2026-07-26 and all failed:

| URL | Status |
| --- | --- |
| `https://developer.console.com.au/` | 000 (DNS does not resolve) |
| `https://developers.console.com.au/` | 000 (DNS does not resolve) |
| `https://docs.console.com.au/` | 000 (DNS does not resolve) |
| `https://console.com.au/developers` | 404 |
| `https://console.com.au/api` | 404 |
| `https://console.com.au/docs` | 404 |
| `https://api.console.com.au/` | 404 (host answers, nothing published) |
| `https://api.console.com.au/openapi.json` | 404 |
| `https://api.console.com.au/swagger.json` | 404 |
| `https://api.console.com.au/api-docs` | 404 |
| `https://api.console.com.au/graphql` | 404 |
| `https://www.console.com.au/$metadata` | 404 |
| `https://www.console.com.au/.well-known/openid-configuration` | 404 |

The full `sitemap.xml` (200, ~85 URLs) contains no developer-facing page at all.

## RESO Posture

**Not certified. No RESO reference found.**

Australia has no MLS. The residential market is a portal duopoly — REA Group's
realestate.com.au and Domain — sitting over state land registries, with PEXA as
the electronic conveyancing rail and PropTrack and CoreLogic supplying valuation
data. RESO is a North American, NAR-driven construct, so there is no cooperative
database for an Australian vendor to certify against.

- RESO Web API certification: none found
- RESO Data Dictionary certification: none found (no version)
- RESO certification directory listing: none found
- OData endpoints: none found
- `$metadata` document: none served
- Universal Property Identifier (UPI): not present

A case-insensitive grep for RESO, Data Dictionary, OData, UPI and Universal
Property Identifier across the fetched console.com.au pages and the parent group's
entire developer documentation corpus returned zero substantive matches.

## Access Gate

**`partner-only`** — and gated.

Console Group runs a live integration marketplace at
[/integrate](https://www.console.com.au/integrate) listing more than twenty
third-party products (MyConnect, Tapi, Inspection Express, Bricks + Agent, Snug,
DEFT, REI Forms Live, Property Inspection Manager, Inspection Manager, Move Me In,
FastConnect, YourPorter, Compare and Connect, Movinghub, plus native Reapit PM
Inspect, Console Pay, Reapit Sales, InspectRealEstate and Agentbox). Those
integrations cannot exist without an API — but the page carries no developer
documentation, no API mention and no "become an integration partner" form. The
[/partners](https://www.console.com.au/partners) page lists ten certified
**training** partners for property managers, not technology partners.

**What a developer must sign or join:** nothing is published. The only route to
the company is the generic contact and demo forms, so entry is a privately
negotiated commercial arrangement. There is no self-serve signup, no application
form, no published developer terms, no sandbox and no keys.

## Open Data

**None.** Console Group is a private SaaS vendor holding its customers' trust
accounting, tenancy and rent-roll data. Australia's open property counterweight
sits with government — state land registries, the ABS and data.gov.au — not with
property management software vendors.

## Auth Model

**None published by Console Group.** `/.well-known/openid-configuration` returns
404 on both `www.console.com.au` and `api.console.com.au`, as does
`/.well-known/security.txt`. The `/login` page (200) is an end-user application
login for agency staff, not a developer credential surface: no API keys, no OAuth
client registration and no scopes are documented anywhere.

For context only, the parent group operates **Reapit Connect**, an Auth0-backed
OpenID Connect provider whose discovery document at
`https://connect.reapit.cloud/.well-known/openid-configuration` is served
anonymously (200, `application/json`). Nothing in the parent's documentation ties
it to Console Cloud / Reapit PM, so it is recorded as context in `review.yml` and
is **not** attributed to Console Group.

## Webhooks, Events, SDKs, Postman

Absence is the finding. Console Group publishes no webhooks, no event catalog, no
SDKs or packages, no Postman collections, no CLI, no GraphQL endpoint, no MCP
server and no sandbox. The
[product updates](https://www.console.com.au/product-updates) page is end-user
release notes, not an API changelog — captured in
[`changelog/console-group-changelog.yml`](changelog/console-group-changelog.yml).

It does, however, run a real public **status page** at
[status.console.com.au](https://status.console.com.au/) — a Hund.io page with Cloud
and Accounts components, published percent-uptime and response-time metrics and an
on-page incident history. Its HAL+JSON API at `/api/v1` returns 401 anonymously, so
there is no machine-readable status feed. This was found in the 2026-07-26 enrichment
round and corrects the bootstrap review, which reported no status page after probing
only console.com.au paths.

## Product API Family

None of these are exposed as documented APIs. They are recorded so the real shape
of the platform, in the segmentation the company's own site uses, is on file.

| Segment | Products |
| --- | --- |
| Property management & trust accounting | Console Cloud / Reapit PM |
| Inspections | Console Go + Inspect |
| Maintenance | Maintenance / Maintenance Pro |
| Payments | Console Pay |
| Commercial property | Commercial |
| Analytics & reporting | Analytics+ |
| Owner & tenant experience | Owner Portal, Tenant App |
| Communications | Console SMS |
| Sales CRM (sibling product) | Console Sales / Reapit Sales (Agentbox) |

## Parent Company Caveat

Reapit, the UK parent, **does** operate a genuine developer platform — Reapit
Foundations, with public documentation, a registration form, OpenID Connect
authentication, REST, GraphQL, webhooks and an alpha MCP server. It would be
wrong to credit that to Console Group. A grep across the entire Foundations
documentation corpus for *Console*, *Console Cloud*, *Reapit PM*, *Australia*,
*New Zealand* and *ANZ* returned **zero** matches — Foundations documents the UK
AgencyCloud line, not the ANZ Console platform. Reapit is profiled separately.
Even Foundations' own Swagger document is 401-gated at `platform.reapit.cloud`,
so no machine-readable contract was harvestable from either company.

## Properties

- [Website](https://www.console.com.au/)
- [Product](https://www.console.com.au/cloud)
- [Marketplace](https://www.console.com.au/integrate)
- [Pricing](https://www.console.com.au/pricing)
- [Support](https://www.console.com.au/support)
- [Help Center](https://help.console.com.au/)
- [Change Log](https://www.console.com.au/product-updates)
- [Blog](https://www.console.com.au/blog)
- [Case Studies](https://www.console.com.au/case-studies)
- [About](https://www.console.com.au/about-us)
- [Contact](https://www.console.com.au/contact-us)
- [Sign Up](https://www.console.com.au/book-a-demo)
- [Login](https://www.console.com.au/login)
- [Terms of Service](https://www.console.com.au/terms-of-use)
- [Privacy Policy](https://www.console.com.au/privacy-statement)
- [LinkedIn](https://au.linkedin.com/company/console-australia-new-zealand)
- [Parent Company](https://www.reapit.com/)

## Maintainers

- Kin Lane — kin@apievangelist.com

## Enrichment round 2026-07-26

Artifacts added this round, all from live probes or the company's own pages — nothing
invented:

| Artifact | What it records |
| --- | --- |
| [`lifecycle/`](lifecycle/console-group-lifecycle.yml) | The newly-found status page, its components and metrics, the 401-gated Hund API, and the absence of any versioning, deprecation or SLA policy |
| [`changelog/`](changelog/console-group-changelog.yml) | Eight dated product releases (Aug 2024 – May 2025) from /product-updates, flagged as end-user notes, not an API changelog |
| [`integrations/_index.yml`](integrations/_index.yml) | All 21 marketplace listings, every one `pending-provider-spec` — no Arazzo is possible without a Console-side contract |
| [`well-known/`](well-known/console-group-well-known.yml) | Every `/.well-known/` probe across www, api, app, pm, sso — all 404 or 301, nothing saved |
| [`conformance/`](conformance/console-group-conformance.yml) | Privacy Act 1988 / APP adherence and TLS in transit are the only claims; PCI DSS, SOC 2, ISO 27001, RESO and OData are absent |
| [`packages/`](packages/console-group-packages.yml) | No first-party client library anywhere; the `@reapit/*` npm namespace belongs to the parent and is deliberately not attributed here |
| [`security/`](security/console-group-domain-security.yml) | TLS/HSTS across eight Console hosts, plus DNSSEC/CAA/SPF/DMARC on console.com.au |
| [`llms/`](llms/console-group-llms.txt) | Generated llms.txt (the site serves none) |

