# Kraken Technologies (kraken-technologies)

Kraken Technologies is the United Kingdom energy technology company behind Kraken, the licensed cloud operating system for utilities. Founded in 2016 inside Octopus Energy and spun out as an independent business, Kraken says it supports more than 90 million customer accounts for licensees including E.ON Next, EDF, Origin, Tokyo Gas, National Grid, Good Energy, Plenitude, Energy Queensland, Essential Energy, Portsmouth Water and TalkTalk across electricity, gas, water and broadband. It sits one layer behind the utility rather than in front of the consumer: it does not hold a supply licence, does not settle in the wholesale market and does not publish grid or market data, so the retailers and networks it powers carry the regulatory obligations, not Kraken. Its API posture matches that position and is honestly closed. The Open Kraken programme publicly advertises APIs, events, embedded apps, Flow automation and an MCP-based AI access layer, but every reference surface is gated: docs.kraken.tech forces SSO login on every path, no base URL or endpoint is published anywhere, the Tako design-system package requires a private npm token issued by email, and the Marketplace runs under signed access-and-use terms. There is no self-serve developer signup, no consumer data-portability API of its own, and no open market data.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kraken-technologies/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kraken-technologies/refs/heads/main/apis.yml)

## Tags

- Energy
- United Kingdom
- Utilities
- Electricity
- Gas
- Smart Metering
- Demand Response
- DER
- Billing
- Energy Platform

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

### Open Kraken APIs and Events

Open Kraken is the integration layer of the Kraken utility operating system. Kraken publicly describes it as "APIs, events and MCP" for building apps and experiences against data and capabilities inside Kraken and for bringing data in from a licensee's own apps and third-party tools, alongside the Flow drag-and-drop automation tool and Embedded Apps that render inside the Kraken agent desktop. No base URL, endpoint list, authentication scheme or machine-readable contract is published anywhere on the public web. The reference documentation at docs.kraken.tech returns an SSO login wall on every path probed on 2026-07-27, including `/openapi.json`, `/llms.txt` and `/.well-known/openid-configuration`, each of which redirects to `/auth/login/` and serves `text/html` rather than a spec. Access is available only to Kraken licensees and contracted partners.

- **Human URL:** [https://www.kraken.tech/open-kraken](https://www.kraken.tech/open-kraken)
- **Base URL:** none published

#### Tags

- Energy
- Utilities
- Integration
- Events
- Embedded Apps

#### Properties

- [Documentation](https://www.kraken.tech/open-kraken)
- [Documentation](https://docs.kraken.tech/) — SSO-gated
- [ChangeLog](https://www.kraken.tech/product-updates)

### Open Kraken AI Access Layer (MCP)

An AI access layer that Kraken announced as an expansion of Open Kraken, built using the Model Context Protocol and described as MCP gateways that let a utility's own AI agents orchestrate approved actions across Kraken, with fair use included. Kraken states the layer is being gradually released. No MCP server URL, tool list, scope model or transport is published; a probe of `mcp.kraken.tech` on 2026-07-27 did not resolve. MCP is the only protocol Kraken names for this surface, and it is an agent-integration protocol rather than an energy data standard.

- **Human URL:** [https://www.kraken.tech/open-kraken](https://www.kraken.tech/open-kraken)
- **Base URL:** none published

#### Tags

- Energy
- MCP
- AI Agents
- Utilities

#### Properties

- [Documentation](https://www.kraken.tech/open-kraken)
- [Announcement](https://www.kraken.tech/press-releases/kraken-expands-open-kraken-with-ai-access-layer-and-marketplace)
- [Documentation](https://docs.kraken.tech/) — SSO-gated

## Regulatory Posture

- **Mandate regime:** none — Kraken is a technology vendor, not a licensed supplier, network operator or accredited data recipient. Great Britain's Smart Energy Code / DCC obligations, Elexon's Balancing and Settlement Code and the Ofgem supply licence bind Kraken's licensees, not Kraken.
- **Mandate status:** not-applicable. Kraken makes no public compliance claim, so there was no claim to downgrade.
- **Australian CDR check:** the public CDR register (`GET https://api.cdr.gov.au/cdr-register/v1/all/data-holders/brands/summary`, HTTP 200, 203 brands, 2026-07-27) returns zero Kraken entries, even though Origin Energy, Energy Queensland and Essential Energy run on Kraken.
- **Data standard:** no standard reference found. No Green Button/ESPI, CDR Consumer Data Standards, OCPP/OCPI, OpenADR, IEEE 2030.5 or IEC CIM. The only protocol named is MCP.
- **Consumer data API:** no. The consumer-facing Kraken-backed surface belongs to the licensee — see [developer.octopus.energy](https://developer.octopus.energy/), profiled separately as `octopus-energy`.
- **Open market data:** no. Kraken operates no grid, market or emissions feed; in its home market those belong to NESO, Elexon and the DNOs.
- **Access gate:** partner-only. A developer needs a Kraken licence or partner contract, then SSO credentials for docs.kraken.tech, then an emailed private-npm token from `tako@kraken.tech` to build Embedded Apps.
- **Auth model:** not published. No API key format, OAuth2 flow, scope model or mTLS profile is documented anonymously.

## Common Properties

- [Website](https://www.kraken.tech/)
- [Documentation](https://docs.kraken.tech/)
- [Design System](https://tako.kraken.tech/)
- [SDK](https://github.com/kraken-tech/kraken-apps-examples)
- [GitHub Organization](https://github.com/kraken-tech)
- [GitHub Organization](https://github.com/octoenergy)
- [LinkedIn](https://www.linkedin.com/company/krakentech/)
- [Blog](https://www.kraken.tech/insights)
- [Press Releases](https://www.kraken.tech/press-releases)
- [ChangeLog](https://www.kraken.tech/product-updates)
- [Partners](https://www.kraken.tech/marketplace)
- [Partner Program](https://www.kraken.tech/bpo-partner-program)
- [Vulnerability Disclosure](https://www.kraken.tech/vulnerability-disclosure-process)
- [Trust Center](https://www.kraken.tech/legal/trust-center)
- [Terms of Service](https://www.kraken.tech/legal/marketplace-access-and-use-terms)
- [Privacy Policy](https://www.kraken.tech/legal/privacy-notice)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
