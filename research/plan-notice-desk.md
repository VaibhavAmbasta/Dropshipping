# Plan: a tool for CA firms that catches GST and TDS mismatches before notices arrive

Fit: tech + finance. Customer: small CA firms (5–20 staff) handling 50–300 client GSTINs each.

## Why sell to CA firms, not to business owners
- **One sale covers many clients.** One CA firm brings 50–300 businesses. Selling to business owners one by one is slow and expensive.
- **Signing isn't your problem.** You don't need to be a CA, because the CA signs the replies.
- **The pain is in their office.** Data-driven GST scrutiny means more notices (ASMT-10, DRC-01), and the Income Tax Act 2025 changed every TDS section code from 1 Apr 2026. CA staff time is the bottleneck.

## What it does (MVP)
1. **Upload files instead of using APIs.** Start with files exported from the GST portal (GSTR-1, 2B/IMS, 3B) and from Tally or Excel books. Connecting to the portals directly needs a licensed partner later: a GSP for GST data and ERI registration for income-tax data.
2. **Mismatch report for each client:** ITC claimed vs 2B, turnover across GSTR-1, 3B and books, missing supplier filings, and reverse-charge gaps. Each line comes with an estimated amount at risk.
3. **Notice tracker:** one dashboard across every client, showing notices, due dates and reply status.
4. **Free lead tool:** a public web tool that maps old TDS sections to the new ones. It's timely, and it brings CAs to you.

## Pricing hypothesis
₹3–10k per firm per month, or about ₹100–200 per client GSTIN per month. Test it in conversations. Don't guess.

## First 30 days
| Week | Do | Done when |
|---|---|---|
| 1 | Talk to 20 CA firms (LinkedIn, ICAI branch meetings, people you know). Ask how many notices they get a month, how many hours each reply takes, what tools they use, and what they'd pay. **Write no code** | 20 calls logged |
| 2 | Concierge MVP: run reconciliations for 2 firms by hand plus Python scripts on their real exports. Charge even ₹5k | 1 firm pays |
| 3–4 | Build upload → reconcile → report → tracker. Ship the free TDS section mapper | 3 firms using it weekly |

**Stop or pivot if:** fewer than 3 of the 20 CAs say they would pay, *and* nobody pays for the manual version. In that case, move to the health-claim file-check idea (`india-domestic-ideas.md` #2).

## Known competition
ClearTax, Suvit, IRIS, GSTHero, Computax, Zoho and Tally all reconcile in some form. **You win on the notice-prevention workflow across all clients and on speed of setup for small firms, not on reconciliation alone.** If the calls show that existing tools already solve this, believe the calls.

## Data security
You'll hold financial data for hundreds of businesses. The DPDP Act applies to you too. Encrypt everything, keep each firm's data separate, and set up proper access logs from day one.
