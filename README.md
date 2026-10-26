# People First Bank (people-first-bank)

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

People First Bank is an Australian customer-owned mutual bank, the trading name of Heritage and People's Choice Ltd (ABN 11 087 651 125), formed from the 2023 merger of Heritage Bank and People's Choice Credit Union. B Corp certified and member-owned, it offers everyday banking, lending, and insurance nationally. Under Australia's Consumer Data Right (CDR / open banking) it publishes a public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body Consumer Data Standards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/people-first-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/people-first-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Mutual Bank
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### People First Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right (CDR) Product Reference Data API exposing the bank's banking product catalogue. Confirmed live at `https://public.openbanking.peoplefirstbank.com.au/cds-au/v1/banking/products` (HTTP 200, x-v 5) returning a `data.products` array, with a Get Product Detail endpoint at `/banking/products/{productId}`. Conforms to the Data Standards Body Consumer Data Standards Get Products specification; no bank-proprietary OpenAPI is published, so the shared DSB CDS Banking contract is harvested here.

- **Human URL:** [https://www.peoplefirstbank.com.au/help-and-support/open-banking/open-banking-for-developers](https://www.peoplefirstbank.com.au/help-and-support/open-banking/open-banking-for-developers)
- **Base URL:** `https://public.openbanking.peoplefirstbank.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://www.peoplefirstbank.com.au/help-and-support/open-banking/open-banking-for-developers)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/people-first-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.peoplefirstbank.com.au/)
- [Developer Portal](https://www.peoplefirstbank.com.au/help-and-support/open-banking/open-banking-for-developers)
- [Documentation](https://www.peoplefirstbank.com.au/help-and-support/open-banking)
- [LinkedIn](https://www.linkedin.com/company/people-first-bank)
- [Blog](https://www.peoplefirstbank.com.au/help-and-support/blog)
- [Privacy Policy](https://www.peoplefirstbank.com.au/privacy)
- [Terms of Service](https://www.peoplefirstbank.com.au/disclaimer)
- [Support](https://www.peoplefirstbank.com.au/help-and-support/contact-us)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
