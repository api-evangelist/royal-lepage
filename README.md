# Royal LePage (royal-lepage)

Royal LePage is Canada's largest residential real estate brokerage brand, founded in Toronto in 1913 as A.E. LePage and operated today under franchise and corporately-owned brokerages by Bridgemarq Real Estate Services (TSX: BRE), an affiliate of Brookfield. It spans roughly 20,000 licensed REALTORS across 600-plus offices nationwide, and sits in the value chain as a brokerage/franchisor rather than as a data platform. Its consumer search at royallepage.ca is a downstream CONSUMER of listing data, not a publisher of it — the site states its inventory is "226,755 active MLS listings via the CREA DDF network," meaning the machine-readable feed belongs to the Canadian Real Estate Association's Data Distribution Facility, not to Royal LePage. On API posture the honest finding is that there is none published for developers — no developer portal, no documented API, no OpenAPI or OData `$metadata`, no RESO Web API or Data Dictionary certification anywhere in evidence, and no SDKs, webhooks, or Postman collections.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/royal-lepage/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/royal-lepage/refs/heads/main/apis.yml)

## Tags

- Real Estate
- Canada
- Property Listings
- MLS
- Brokerage
- IDX
- VOW
- Residential Real Estate
- Franchise
- PropTech

## Timestamps

- **Created:** 2026-07-26
- **Modified:** 2026-07-26

## APIs

None. Royal LePage publishes no documented public API. `apis[]` is intentionally empty — see `review.yml` for every URL probed and its HTTP status.

## RESO Posture

**No RESO reference found. Not certified.**

There is no RESO Web API certification, no RESO Data Dictionary certification (no 1.7, no 2.0), no entry in the RESO certification directory, no `Reso`/OData endpoint, no `$metadata` document, and no use of the RESO Universal Property Identifier (UPI). This is structural rather than an omission: RESO certification is organised around US MLSs under NAR, while Canadian residential listing syndication runs through CREA's single national Data Distribution Facility (DDF), which Royal LePage consumes as a licensee. A brokerage brand is not the certifying party in either regime.

## Access Gate

**`none-published`** — gated.

A developer has nothing to sign with Royal LePage, because there is no developer programme. The real gates sit underneath:

1. **Consumer (VOW).** Registering an account on royallepage.ca "creates a Virtual Office Website (VOW) relationship between Royal LePage Real Estate Services, Brokerage and the Registrant," and the data is "only for the Registrant's personal, non-commercial use."
2. **Automated access prohibited.** The legal notice forbids "spiders, robots, crawlers, data mining tools, or the like." There is no API carve-out.
3. **The data seam is CREA, not Royal LePage.** The site footer states the property information "is derived from Royal LePage listings and the Canadian Real Estate Association's Data Distribution Facility (DDF)." Programmatic access to that record goes through CREA membership and a DDF licence.
4. **Agents and franchisees.** rlpnetwork.com is a members-only login wall.

## Open Data

**No.** Royal LePage publishes recurring market research (House Price Survey / National House Price Composite and seasonal reports) as HTML narrative and chart pages — no CSV, no JSON, no API, and it is copyrighted research rather than an open dataset. Canadian land registration is provincial and largely privatised (Teranet holds long concessions in Ontario), so the public record downstream of this brand is itself a commercial product.

## Auth Model

- **Developer:** none — no keys, OAuth clients, or scopes are issued or documented.
- **Consumer:** email/password account creation with emailed verification code, plus "Log in with Facebook" and "Log in with Google" buttons.
- **Member:** rlpnetwork.com WordPress form login. No OpenID Connect discovery document is served; `/.well-known/openid-configuration` redirects to `/login`.

## Webhooks, Events, SDKs, Postman

None found — the absence is the finding. There is no GitHub organization; a GitHub **user** account [RoyalLePage](https://github.com/RoyalLePage) exists with 0 public repositories.

## Properties

- [Website](https://www.royallepage.ca/en/)
- [About](https://www.royallepage.ca/en/realestate/about-us/)
- [Parent Company](https://www.bridgemarq.com/)
- [Portal — rlpNetwork (members only)](https://www.rlpnetwork.com/)
- [Newsroom](https://www.royallepage.ca/en/realestate/about-us/media-room/)
- [Research — House Price Survey](https://www.royallepage.ca/en/realestate/house-prices/)
- [Terms of Service](https://www.royallepage.ca/en/realestate/legal-notice/)
- [Privacy Policy](https://www.royallepage.ca/en/realestate/privacy-policy/)
- [LinkedIn](https://ca.linkedin.com/company/royal-lepage)
- [GitHub Profile](https://github.com/RoyalLePage)

## Maintainers

- Kin Lane — kin@apievangelist.com
