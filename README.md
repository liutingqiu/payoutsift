# PayoutSift

PayoutSift is an offline payout reconciliation and audit report kit for independent sellers, freelancers, bookkeepers, and small online businesses.

It compares three mapped CSV exports:

```text
transactions -> processor payouts -> bank deposits
```

The paid tool produces a self-contained HTML report, JSON audit record with SHA-256 input fingerprints, payout reconciliation CSV, row-level exception queue, normalized transactions, and unmatched deposit list. It runs locally with Python 3.10+ and has no third-party packages, API keys, cloud uploads, analytics, or recurring fee.

## Live demo

- [Product page and report preview](https://liutingqiu.github.io/payoutsift/)
- [Download the fictional evaluation demo](https://github.com/liutingqiu/payoutsift/releases/latest)

The demo intentionally includes duplicate, orphan, difference, ambiguity, missing-source, and unmatched-deposit cases. It contains generated reports and fictional inputs, not the paid reconciliation engine.

## What PayoutSift checks

- transaction net arithmetic (`gross - fees - refunds`);
- duplicate and conflicting transaction, payout, and deposit IDs;
- missing payout sources and orphan transactions;
- transaction net totals versus payout amounts;
- one-to-one bank deposit matches by currency, tolerance, and settlement window;
- ambiguous and unmatched bank deposits;
- strict currency isolation;
- source file fingerprints and row-level review evidence.

## Scope

Version 1 uses three documented fixed schemas. It does not connect to a payment processor or bank, move money, convert currencies, calculate tax, post accounting entries, or replace accounting review.

## Current purchase status

The commercial package is available for [USD 19 one-time on Payhip](https://payhip.com/b/DjJEw) for one business. This repository does not claim an order, sale, or revenue; those require a real purchase that has completed and settled.

Copyright 2026 ZAKU. The evaluation demo has its own license inside the download; the paid software is not distributed from this repository.
