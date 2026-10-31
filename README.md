# Roblox

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Roblox is a user-generated content platform where creators build, publish, and monetize immersive 3D experiences using Roblox Studio and the Luau scripting language. Roblox exposes three distinct developer surfaces: the in-engine Luau scripting API (Roblox Engine API) running inside experiences and Studio plugins, the Roblox Studio plugin API for editor tooling, and the Open Cloud API (apis.roblox.com) for external programmatic access from servers, build pipelines, and back-office tools. The Open Cloud surface covers DataStores, Memory Stores, Messaging Service, Place Publishing, Universes, Assets, Inventory, Users, Groups, Notifications, Subscriptions, and Luau Execution, authenticated either with API keys scoped per-resource or with OAuth 2.0 for third-party apps. Roblox also publishes deep documentation for the Engine API at create.roblox.com/docs and the legacy ROBLOX Web APIs that power the website (subdomains such as users.roblox.com, groups.roblox.com, inventory.roblox.com), which remain undocumented for third parties.

**Areas:** Assets · Datastores · Game Development · Games · Luau · Messaging · Open Cloud · Roblox · Scripting · Studio · UGC · Universes

## Roblox on APIs.io

Everything profiled for Roblox is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/roblox/](https://apis.io/providers/roblox/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Roblox Open Cloud API](https://apis.io/apis/roblox/roblox-open-cloud-api/) — The Roblox Open Cloud API is the official external REST surface for Roblox creators, studios, and partners. It exposes universes, places, place publishing,…
- [Roblox Open Cloud Data Stores](https://apis.io/apis/roblox/roblox-open-cloud-datastores/) — The Data Stores Open Cloud API reads and writes persistent key-value data for an experience from outside the engine, including standard data stores and…
- [Roblox Open Cloud Messaging Service](https://apis.io/apis/roblox/roblox-open-cloud-messaging-service/) — The Messaging Service Open Cloud API publishes messages to a topic that running game servers can subscribe to via the in-engine MessagingService class,…
- [Roblox Open Cloud Place Publishing](https://apis.io/apis/roblox/roblox-open-cloud-place-publishing/) — The Place Publishing Open Cloud API uploads .rbxl or .rbxlx files to a place in a universe and either saves or publishes the new version, enabling CI/CD…
- [Roblox Open Cloud Assets](https://apis.io/apis/roblox/roblox-open-cloud-assets/) — The Assets Open Cloud API creates, updates, and reads assets (audio, decals, images, models, mesh parts) on behalf of a user or group, used by asset…
- [Roblox Engine API (Luau)](https://apis.io/apis/roblox/roblox-engine-api-luau/) — The Roblox Engine API is the in-engine scripting surface used inside experiences and Studio plugins. It is written in Luau, Roblox's typed dialect of Lua…
- [Roblox Studio Plugin API](https://apis.io/apis/roblox/roblox-studio-plugin-api/) — The Roblox Studio Plugin API is a superset of the Engine API available to plugins running inside Roblox Studio. It exposes plugin-only services for…
- [Roblox OAuth 2.0](https://apis.io/apis/roblox/roblox-oauth2/) — Roblox OAuth 2.0 lets third-party applications authenticate Roblox users and obtain scoped access tokens to call permitted Open Cloud resources on the…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/roblox/](https://apis.io/graphqls/roblox/roblox-graphql/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Roblox — creator docs rules](https://apis.io/rules/roblox/roblox-creator-docs-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Roblox Domain Security](https://apis.io/security/roblox/roblox-domain-security/)
- [Roblox Vulnerability Disclosure](https://apis.io/security/roblox/roblox-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Roblox Plans Pricing](https://apis.io/plans/roblox/roblox-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Roblox Rate Limits](https://apis.io/rate-limits/roblox/roblox-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Roblox Finops](https://apis.io/finops/roblox/roblox-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.roblox.com)
- [Documentation](https://create.roblox.com/docs)
- [API reference](https://create.roblox.com/docs/cloud/reference)
- [Support](https://en.help.roblox.com)
- [Blog](https://blog.roblox.com)
- [Terms of service](https://www.roblox.com/info/terms)
- [Privacy policy](https://www.roblox.com/info/privacy)
- [GitHub](https://github.com/Roblox)

## API Evangelist rating

**Kin Score 28.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 0.0 |
| Contract governance | 45.5 |
| Operational transparency | 10.5 |
| Developer ergonomics | 33.3 |
| Access clarity | 26.3 |

**Agent readiness 3.1** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 25.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/roblox/](https://apis.io/providers/roblox/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Roblox: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/roblox/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
