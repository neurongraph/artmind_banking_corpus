### Entity: Interest Rate  
**Definition:** A specific rate of interest applied to accounts.  
**Attributes:**
- `rate_id` — Unique identifier
- `product_id` — Linked product
- `rate_type` — Fixed, Variable, Tiered
- `rate_value` — Annual percentage (e.g., 4.5)
- `rate_tier` — Balance threshold (e.g., £0–£10,000)
- `effective_date` — When rate became effective
- `next_review_date` — Planned rate review date
- `review_basis` — Linked to Bank of England base rate, margin  
**Example:**
```
Interest Rate:
- product_id: SAV-001
- rate_type: Tiered Variable
- Tier 1: £0–£10,000 @ 4.5% AER
- Tier 2: £10,001–£50,000 @ 4.7% AER
- Tier 3: £50,001+ @ 4.8% AER
- review_basis: BoE base rate + 2.5% margin
- effective_date: 2026-01-15
```  
---