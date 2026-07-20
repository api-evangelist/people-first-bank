---
name: Look up People First Bank banking products
description: Discover and inspect the banking products People First Bank openly offers to the market via the public CDR Product Reference Data API — no authentication required.
api: openapi/people-first-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
---

# Look up People First Bank banking products

People First Bank exposes a public, **unauthenticated** Consumer Data Right (CDR)
Product Reference Data (PRD) API. Use it to browse the bank's openly-offered
products and drill into a single product's fees, rates, features, and eligibility.
No API key, OAuth token, or CDR accreditation is needed for these two operations.

Base URL: `https://public.openbanking.peoplefirstbank.com.au/cds-au/v1`

## Rules (read before calling)

- **Version header is required.** Every request MUST send an `x-v` header (a positive
  integer). Use `x-v: 5` for `listBankingProducts` and `x-v: 7` for
  `getBankingProductDetail`. An unsupported version returns **406 Unsupported Version**.
- **Read-only.** Both operations are `GET`. There is no idempotency-key contract because
  nothing is mutated.
- **Errors** come back as `{ "errors": [ { code, title, detail } ] }` with `urn:au-cds:...`
  codes — not RFC 9457 problem+json. See `errors/people-first-bank-problem-types.yml`.
- Optionally send `x-fapi-interaction-id` (an RFC 4122 UUID); the server echoes it back for
  correlation.

## Steps

1. **List products** — call `listBankingProducts` (`GET /banking/products`) with `x-v: 5`.
   - Narrow with query params: `product-category` (e.g. `RESIDENTIAL_MORTGAGES`,
     `TERM_DEPOSITS`, `TRANS_AND_SAVINGS_ACCOUNTS`), `effective` (`CURRENT` default /
     `FUTURE` / `ALL`), `brand`, and `updated-since` (only products changed after a
     timestamp).
   - Paginate with `page` (default 1) and `page-size` (default 25); read `meta.totalPages`
     and the `links.next` cursor to walk all pages.
   - Each item carries a `productId`, `productCategory`, `name`, and `lastUpdated`.

2. **Get product detail** — for a `productId` of interest, call `getBankingProductDetail`
   (`GET /banking/products/{productId}`) with `x-v: 7`.
   - Read the arrays `features`, `constraints`, `eligibility`, `fees` (each fee may carry
     `discounts`), `depositRates`, and `lendingRates` (rates carry `tiers` →
     `applicabilityConditions`).
   - A `404` (`Resource/Invalid` or `Resource/Unavailable`) means the `productId` is no
     longer offered — re-run step 1 to refresh the catalogue.

## Notes

Consumer account/transaction data (balances, transactions, payees, direct debits, scheduled
payments) is **not** part of this public surface — it requires the CDR accredited-data-recipient
model (OAuth2/OIDC under the FAPI profile via the CDR register) and cannot be reached with these
two public operations.
