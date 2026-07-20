# People First Bank (people-first-bank)

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
