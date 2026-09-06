## 2. Product Domain  
### Entity: Product  
**Definition:** A financial service offered by FirstUK Bank (see [[products]]).  
**Attributes:**
- `product_id` — Unique identifier (e.g., "SAV-001")
- `product_name` — Marketing name (e.g., "SmartSaver Account")
- `product_type` — Savings, Current, Mortgage, Card
- `description` — Product description
- `launch_date` — Product launch date
- `status` — Active, Inactive, Deprecated
- `min_balance` — Minimum opening balance (if applicable)
- `max_balance` — Maximum balance limit (if applicable)
- `target_customer` — Target market segment  
**Relationships:**
- `has_features` → Feature (1:many)
- `has_pricing_tier` → PricingTier (1:many)  
**Example:**
```
Product: SmartSaver Account
- product_id: SAV-001
- product_type: Savings
- min_balance: £1
- target_customer: General consumers, ages 18+
```  
---